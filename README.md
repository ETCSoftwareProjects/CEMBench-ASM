> ## ⚠️ Important Notice
>
> In accordance with the applicable regulations of the **Republic of Türkiye concerning public officials and restrictions on commercial and other income-generating activities**, this repository will remain temporarily available. During this period, public access to the software and related materials is maintained solely for **academic and scientific purposes**.
>
> Once the institutional portal currently under development has become operational, CEMBench ASM and its related academic and educational materials will be moved to that portal. This repository will then be retained only to redirect visitors to the portal.
>
> **CEMBench ASM is developed and distributed free of charge for academic and educational purposes. No fees, advertising revenue, donations, sponsorship income, subscription revenue, or other income is generated through the distribution of CEMBench ASM via this GitHub repository, and no such payments or contributions will be accepted.**

---


# CEMBench ASM

**Model development and simulation software for activated sludge processes**

CEMBench ASM is a configurable model-development, simulation, and analysis environment for activated sludge processes. It combines a visual treatment-process topology with template-defined components, aggregates, parameters, processes, rate expressions, mappings, and Gujer-matrix relationships.

CEMBench ASM is intended primarily for undergraduate and graduate education, model development, and non-commercial academic investigation. The signed educational templates supplied with the installer range from introductory substrate–biomass and carbon-removal models to the ASM1, ASM2d, ASM3, and ASM3p models.

## Download

Download the current installer, release notes, EULA, and SHA-256 checksums from the [Releases](../../releases/latest) page. The CEMBench ASM User Manual (PDF) is provided with the [CEMBench ASM 1.0.0 release](../../releases/tag/v1.0.0).

Install CEMBench ASM using:

`CEMBenchASM_<version>_x64.msi`

Do not use the automatically generated GitHub source-code archives as the installer.

## Included Software

The public installer contains:

- CEMBench ASM
- CEMBench ASM Template Editor
- the bundled Verification Report add-in
- the bundled MATLAB Model Export add-in (from release 1.1.0)
- six signed educational templates
- the Quick Start example project

## Included Educational Templates

- Introductory S–X Model
- Introductory C Removal
- ASM1
- ASM2d
- ASM3
- ASM3p

## System Requirements

- 64-bit Windows 10 or Windows 11
- 64-bit processor
- minimum 4 GB RAM
- minimum display resolution of 1600 × 900 pixels

The installer is self-contained. A separate .NET installation is not required.

## License and Permitted Use

CEMBench ASM is distributed as binary-only freeware for non-commercial educational and academic use.

The application source code is not included, and CEMBench ASM is not open-source software. Commercial use, redistribution, repackaging, modification, and reverse engineering are subject to the restrictions stated in the applicable EULA.

Installation and use are governed by the EULA supplied with each release.

## Course Materials

CEMBench ASM educational activities provide structured assignments for teaching and learning activated sludge process concepts through modeling and simulation.

Each activity is described on its own page, which provides the assignment instructions and supporting material. Activity ratings and user feedback are also available through the course-materials collection.

- [Browse CEMBench ASM Course Materials](Course%20Materials)

## Documentation

The CEMBench ASM User Manual (PDF) is published as an asset of the [CEMBench ASM 1.0.0 release](../../releases/tag/v1.0.0). It describes release 1.0.0; changes introduced in later releases are described in the release notes of the corresponding release.

Users should retain the exact CEMBench ASM version, template version, CBM files, and analysis settings used in teaching or research work.

## CEMBench ASM User Rating

Users who have used CEMBench ASM are invited to provide feedback through the common CEMBench ASM User Feedback survey.

The public rating is based only on the response to:

> **Overall, how would you rate CEMBench ASM?**

Ratings use a five-point scale. To avoid displaying unstable ratings based on very small numbers of responses, a public rating is shown only after at least **10 responses** have been collected. Other survey responses are not published on this page.

<!-- CEMBENCHASM_RATING_START -->
**Not yet rated**  
**Responses:** 0
<!-- CEMBENCHASM_RATING_END -->

[Provide CEMBench ASM User Feedback](https://docs.google.com/forms/d/e/1FAIpQLScPnSf4UaFd5WfNsERoe8g_Zh7tJe5UAivC4EtMrCoFdbBgtQ/viewform?usp=publish-editor)

## Bug Reports and Feature Requests

Reproducible software problems and suggestions should preferably be submitted through [GitHub Issues](../../issues).

If GitHub Issues cannot be used, they may alternatively be sent by e-mail to the CEMBench ASM development team, **ETC Software Projects**, at [etcsoftwareprojects@gmail.com](mailto:etcsoftwareprojects@gmail.com).

A bug report should include:

- the exact CEMBench ASM version;
- the affected application or module;
- the Windows version;
- the template and general project configuration;
- exact reproduction steps;
- expected behavior;
- observed behavior; and
- screenshots or error messages where available.

Remove confidential, personal, institution-restricted, and plant-specific information before uploading or sending files or screenshots.

The issue tracker and the e-mail address are not intended for project preparation, model calibration, result interpretation, or individual technical support.

Submission does not guarantee an individual response, workaround, correction, update, or release date.

## Scientific Limitations

CEMBench ASM results depend on the selected model, template, assumptions, input data, parameter values, topology, operating conditions, and numerical settings.

CEMBench ASM must not be used as the sole basis for treatment-plant design, construction, equipment selection, regulatory compliance, operational control, environmental protection, safety-related decisions, financial commitments, or other consequential actions.

Users remain responsible for reviewing inputs and outputs and independently verifying important results.

## Releases

All public CEMBench ASM versions are published through this repository.

The release naming convention is:

- Git tag: `v1.0.0`, `v1.0.1`, `v1.1.0`, and so forth
- Release title: `CEMBench ASM 1.0.0`, `CEMBench ASM 1.0.1`, `CEMBench ASM 1.1.0`, and so forth
- Installer: `CEMBenchASM_<version>_x64.msi`

Older releases remain available for reproducibility and compatibility review.

## Important Notice About GitHub Archives

GitHub automatically displays `Source code (zip)` and `Source code (tar.gz)` files for each release.

These archives contain only the public files committed to this repository. They do not contain the CEMBench ASM application source code and must not be used as the CEMBench ASM installer.
