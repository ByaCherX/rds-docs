---
title: "Universal CRT deployment"
description: "Learn how, when, and where to deploy the Universal CRT library for your app."
ms.date: 10/23/2020
helpviewer_keywords: ["deploying the CRT [C++]", "application CRT deployment [C++]"]
---
# Universal CRT deployment

From Visual Studio .NET through Visual Studio 2013, each major release of the C++ compiler and tools has included a new, standalone version of the Microsoft C Runtime (CRT) library. These standalone versions of the CRT were independent from, and to various degrees, incompatible with each other. For example, the CRT library used by Visual Studio 2012 was version 11, named msvcr110.dll, and the CRT used by Visual Studio 2013 was version 12, named msvcr120.dll. Beginning in Visual Studio 2015, it's no longer the case. Visual Studio 2015 and later versions of Visual Studio all use one Universal CRT.

The Universal CRT (UCRT) is a Microsoft Windows operating system component. It's included as part of the operating system in Windows 10 and Windows Server 2016 or later. The UCRT is available by using Windows Update on older operating systems that are still in extended support. Local deployment of the Universal CRT is supported, with some restrictions.

## Central deployment

The preferred method to centrally install the Universal CRT is to use Microsoft Windows Update. The Universal CRT is a Recommended update for all supported Microsoft Windows operating systems, so by default, most machines install it as part of the regular update process. The initial release of the Universal CRT was [KB2999226](https://support.microsoft.com/kb/2999226). A later update with various bug fixes was made in [KB3118401](https://support.microsoft.com/kb/3118401), and there have been additional updates with further bug fixes and new features. For more recent updates, search [support.microsoft.com](https://support.microsoft.com) for Universal C Runtime or Universal CRT.

Not all Microsoft Windows computers regularly install updates by use of Windows Update, and some may not install all Recommended updates. To support the use of applications built by using the Visual Studio 2015 and later C++ toolsets on those machines, there are Universal CRT redistributable files available for offline distribution. Those redistributable files may be downloaded from one of the KB links above. The Universal CRT redistributable requires that the machine has been updated to the current service pack. So, for example, the redistributable for Windows 7 will only install onto Windows 7 SP1, not Windows 7 RTM.

Because the Universal CRT is a fundamental dependency of the C++ libraries, the Visual C++ redistributable (VCRedist) installs the initial version of the Universal CRT (version 10.0.10240) on machines that don't already have one installed. This version is sufficient to satisfy the C++ library dependencies. If your application depends on a more recent version of the Universal CRT, you must use Windows Update to bring your machine fully up-to-date, or install that version explicitly. It's best to install the Universal C Runtime via Windows Update or an MSU before installing the VCRedist, to avoid potential multiple required reboots.

Not all operating systems are eligible for the most recent Universal C Runtime via Windows Update. On Windows 10, the centrally deployed version matches the version of the operating system. To update the Universal C Runtime further, you must update the operating system. For Windows Vista through Windows 8.1, the latest available Universal C Runtime is currently based on the version included in the Windows 10 Anniversary Update, with additional fixes (version 10.0.14393).

## Local deployment

Local deployment of the Universal CRT is supported, but not recommended for both performance and security reasons. The DLLs for local deployment are included as part of the Windows SDK, in the Windows Kits\\10\\Redist\\ucrt\\DLLs subdirectory, by computer architecture. The DLLs required include ucrtbase.dll and a set of APISet forwarder DLLs named api-ms-win-\*.dll. The set of DLLs required on each operating system varies. It's highly recommended that you include all of the DLLs when you deploy locally.

There are two restrictions on local deployment to be aware of:

- On Windows 10, the Universal CRT in the system directory is always used, even if an application includes an application-local copy of the Universal CRT. It's true even when the local copy is newer, because the Universal CRT is a core operating system component on Windows 10.

- On versions of Windows before Windows 8, the Universal CRT can't be packaged locally with a plugin, if it's located in a directory other than the directory of the main app executable. The APISet forwarder DLLs are unable to resolve the ucrtbase.dll successfully in this case. Some recommended alternative solutions include:

  - Statically link the Universal CRT,
  - Centrally deploy the Universal CRT, or
  - Place the Universal CRT files in the same directory as the app.

## Deployment on Microsoft Windows XP

Visual Studio 2015 and Visual Studio 2017 continue to support development of software for use on Microsoft Windows XP. To support this development, a version of the Universal CRT does work on Microsoft Windows XP. The Microsoft Windows XP operating system is no longer in mainstream or extended support, so central deployment of the Universal CRT onto Microsoft Windows XP is different from other operating systems.

When the Visual C++ redistributable is installed on Windows XP, it directly installs the Universal CRT and all of its dependencies into the system directory. It doesn't install or depend on any Windows Update. The Redistributable merge modules, the Microsoft_VC*version*_CRT_\*.msm files, do the same.

Local deployment of the Universal CRT on Windows XP is the same as on other supported operating systems.

## See also

- [Deployment in Visual C++](deployment-in-visual-cpp.md)
