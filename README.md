> ## ⚠️ Important Notice – Name Change
>
> The name **Procera** has been changed to **CEMBench ASM**. This repository and the software, documentation, and course materials it hosts are now published under the name **CEMBench ASM**.

> ## ⚠️ Important Notice – October 2026
>
> In accordance with the applicable regulations of the **Republic of Türkiye concerning public officials and restrictions on commercial and other income-generating activities** the publicly available YouTube videos related to CEMBench ASM have been removed from public access.
>
> The **CEMBench ASM GitHub repository will remain temporarily available to the public** because the scientific manuscript associated with CEMBench ASM is currently undergoing peer review. During this period, continued public access to the software and the materials referred to in the manuscript is maintained solely for **academic and scientific purposes**.
>
> Once the peer-review process has been completed and the institutional portal currently being developed within **Yıldız Technical University** has become operational, the software releases, documentation, course materials, and other publicly distributed materials hosted in this GitHub repository will be removed.
>
> Thereafter, public access to CEMBench ASM and its related academic and educational materials will be provided through the official institutional infrastructure of **Yıldız Technical University, Republic of Türkiye**. This GitHub repository will then be retained only to redirect visitors to the relevant institutional portal.
>
> **CEMBench ASM is developed and distributed free of charge for academic and educational purposes. No fees, advertising revenue, donations, sponsorship income, subscription revenue, or other income is generated through the distribution of CEMBench ASM via this GitHub repository.**

---


# CEMBench ASM

**Model development and simulation software for activated sludge processes**

CEMBench ASM is a configurable model-development, simulation, and analysis environment for activated sludge processes. It combines a visual treatment-process topology with template-defined components, aggregates, parameters, processes, rate expressions, mappings, and Gujer-matrix relationships.

CEMBench ASM is intended primarily for undergraduate and graduate education, model development, and non-commercial academic investigation. The signed educational templates supplied with the installer support a progressive sequence from introductory substrate–biomass modeling to carbon, nitrogen, and phosphorus removal.

## Download

Download the current installer, user manual, release notes, EULA, and SHA-256 checksums from the [Releases](../../releases/latest) page.

Install CEMBench ASM using:

`CEMBenchASM_<version>_x64.msi`

Do not use the automatically generated GitHub source-code archives as the installer.

## Included Software

The public installer contains:

- CEMBench ASM
- CEMBench ASM Template Editor
- the bundled Verification Report add-in
- four signed educational templates
- the Quick Start example project

## Included Educational Templates

- Introductory S–X Model
- Introductory C Removal
- Introductory CN Removal
- Introductory CNP Removal

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

Each activity may include an assignment workbook, CEMBench ASM project or template files, supporting materials, and a short video briefing. Activity ratings and user feedback are also available through the course-materials collection.

- [Browse CEMBench ASM Course Materials](Course%20Materials)
- [Watch the CEMBench ASM Educational Activity Series on YouTube](https://www.youtube.com/@ETCSoftwareProjects/playlists)

The YouTube videos are activity briefings rather than solution videos. They introduce the purpose and setup of each activity and demonstrate only the initial steps needed to begin the assignment.

## Documentation

Each release includes a version-specific CEMBench ASM User Manual in PDF format.

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

Reproducible software problems and suggestions may be submitted through [GitHub Issues](../../issues).

A bug report should include:

- the exact CEMBench ASM version;
- the affected application or module;
- the Windows version;
- the template and general project configuration;
- exact reproduction steps;
- expected behavior;
- observed behavior; and
- screenshots or error messages where available.

Remove confidential, personal, institution-restricted, and plant-specific information before uploading files or screenshots.

The issue tracker is not intended for project preparation, model calibration, result interpretation, or individual technical support.

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
