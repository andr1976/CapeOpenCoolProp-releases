# CoolProp CAPE-OPEN — Portable Distribution

Public download location for the **portable, no-installer build** of the CoolProp
CAPE-OPEN 1.1 property packages (Windows x64). The source code lives in a separate
repository; this repository only hosts the distributable release artifacts, produced
automatically by that repository's build workflow.

## Download

Get the latest `CoolPropCO-Portable-<version>.zip` from the **[Releases](../../releases)** page.

## What's included

Three CAPE-OPEN 1.1 components (registered per-user, no admin rights):

- **CoolProp Property Package** — PR / SRK / HEOS equations of state, 2-phase VLE, transport properties
- **CoolProp Incompressible** — CoolProp INCOMP fluids (pure or solution), liquid phase
- **CoolProp Package Manager** — factory that lists the packages

The ZIP is self-contained: it bundles `CoolProp.dll`, the Avalonia editor GUI, and the CAPE-OPEN 1.1 PIA.

## Install (per-user, no administrator rights)

1. Download and extract `CoolPropCO-Portable-<version>.zip` to a stable folder you will **not** move, e.g. `%LOCALAPPDATA%\Programs\CoolPropCO`.
2. Run **`register.bat`** (per-user COM registration in HKCU; re-run it if you move the folder — it records the current path).
3. In a CAPE-OPEN simulator (e.g. [COFE / COCO](https://www.cocosimulator.org/)) the packages appear in the property-package list.

To uninstall, run **`unregister.bat`**.

## Prerequisites (target PC)

- Windows x64
- .NET Framework 4.8 or later
- Visual C++ 2015–2022 x64 runtime (`vc_redist.x64.exe`) — required by `CoolProp.dll`

`register.bat` checks these and warns if anything is missing.

## About

Built on [CoolProp](http://www.coolprop.org/) and the [CO-LaN](https://www.colan.org/) CAPE-OPEN 1.1 standard.
