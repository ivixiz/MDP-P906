
# Miniware MDP-P906 Enclosure Reverse Engineering

This repository contains a reverse-engineered 3D model of the **Miniware MDP-P906 programmable power supply enclosure**.

The goal of this project was to recreate the external enclosure dimensions and mechanical features of the original device as accurately as possible in **SolidWorks**, based on measurements of the real hardware.

## Purpose

The generated 3D model can be used as a mechanical reference for designing custom devices that are compatible with the Miniware MDP-P906.
<img width="2560" height="2135" alt="photo_2_2026-06-20_19-07-45" src="https://github.com/user-attachments/assets/61e1627b-9099-4c91-933d-bbb114960bc2" />
<img width="2560" height="2311" alt="photo_1_2026-06-20_19-07-45" src="https://github.com/user-attachments/assets/93c3339f-8cfe-43f5-b42b-452f32d4a23f" />

Potential use cases include:

* Designing custom modules that can stack together with Miniware MDP-P906 power supplies.
* Creating custom enclosures based on the original form factor.
* Mechanical integration and fit-checking during product development.
* Repairing or replacing damaged enclosure parts.
* Educational and reverse-engineering purposes.

## Disclaimer

This model has **not yet been physically 3D printed or verified against a real enclosure** after reconstruction.

While significant effort was made to transfer all dimensions and features as accurately as possible, there is currently **no guarantee that every hole, mounting point, or interface matches the original hardware perfectly**.

Users should verify critical dimensions before manufacturing parts intended for production use.

## Included Files

```text
.
├── Bottom.SLDPRT
├── Bottom.STEP
├── FanMesh.STEP
├── MDP-P906.SLDASM
├── MDP-P906.STEP
├── Top.SLDPRT
└── Top.STEP
```

<img width="837" height="580" alt="image" src="https://github.com/user-attachments/assets/07f083f7-dfbc-44cb-9a22-086072a2c5b9" />

<img width="782" height="495" alt="image" src="https://github.com/user-attachments/assets/609b95f6-1378-43ff-a977-a1a4ccd2ebf8" />

<img width="987" height="665" alt="image" src="https://github.com/user-attachments/assets/f42e63a7-a146-4af3-bb6f-8baf8bac2c06" />

### File Description

| File            | Description                        |
| --------------- | ---------------------------------- |
| Bottom.SLDPRT   | Bottom enclosure part (SolidWorks) |
| Top.SLDPRT      | Top enclosure part (SolidWorks)    |
| MDP-P906.SLDASM | Complete enclosure assembly        |
| Bottom.STEP     | Bottom part in STEP format         |
| Top.STEP        | Top part in STEP format            |
| FanMesh.STEP    | Fan mesh model                     |
| MDP-P906.STEP   | Full assembly exported as STEP     |

## CAD Software

The native project files were created in **SolidWorks**.

For users without SolidWorks, STEP files are provided and can be imported into most CAD software, including:

* FreeCAD
* Fusion 360
* Autodesk Inventor
* Siemens NX
* Solid Edge
* CATIA
* Onshape

## Modifications

The SolidWorks project is intended to be modified and adapted for personal projects. Feel free to:

* Add custom mounting features.
* Modify enclosure dimensions.
* Create compatible expansion modules.
* Design replacement parts.
* Integrate custom electronics.
