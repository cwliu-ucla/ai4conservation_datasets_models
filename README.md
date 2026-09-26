# AI for Conservation Datasets

A curated list of **openly accessible datasets for AI applications in tangible cultural heritage conservation**.

This list accompanies the critical review *How far from practice? An evaluation framework for human-centered AI applications in tangible cultural heritage conservation* (under review at the *Journal of Cultural Heritage*). Every entry comes from a case study analysed in the review. We list a dataset only if its source paper points to a public location (repository, DOI, public collection, or open supplementary material). Datasets offered only "on request" are not included.

The list is organised in two ways:

1. **[By conservation task](#1-datasets-by-conservation-task)**: follows the review's framework of *duty → application*: Examination, Preventive conservation, Treatment and Documentation.
2. **[By heritage type](#2-datasets-by-heritage-type)**: a cross-index for people looking for data on a particular kind of heritage.

---

## Access labels

| Label | Meaning |
|---|---|
| **Open (PID)** | Public download with a persistent identifier (DOI, Zenodo, Figshare, Mendeley Data, IEEE DataPort) |
| **Open** | Public download without a persistent identifier (GitHub, institutional page, cloud-drive link, or journal supplementary material) |
| **Partial** | Only part of the dataset is public, or only the source imagery is public and the authors' annotations are not |
| **Verify** | A public release is claimed, but the paper contradicts itself or the exact link still needs to be confirmed |

> Licences are rarely stated. Unless a licence is given below, check the repository's terms before you redistribute the data or use it commercially.

---

## Summary

| Duty | Application | Datasets listed |
|---|---|---|
| Examination | [Condition diagnosis](#11-condition-diagnosis) | 22 |
| Examination | [Material characterization](#12-material-characterization) | 7 |
| Preventive conservation | [Prediction](#21-prediction) | 1 |
| Preventive conservation | [Risk assessment](#22-risk-assessment) | 4 |
| Treatment | [Cleaning](#31-cleaning) | 0 |
| Treatment | [Structural reconstruction](#32-structural-reconstruction) | 3 |
| Treatment | [Damage/loss inpainting](#33-damageloss-inpainting) | 15 |
| Documentation | [Point cloud segmentation](#41-point-cloud-segmentation) | 2 |
| Documentation | [Photogrammetry / neural 3D reconstruction](#42-photogrammetry--neural-3d-reconstruction) | 0 |

---

## 1. Datasets by conservation task

### Examination

#### 1.1 Condition diagnosis

Detecting, classifying and segmenting deterioration (cracks, spalling, biological growth, efflorescence, paint loss, etc.).

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| Castle of Horst façade bio-colonisation | Built – stone/brick façade | UAV hyperspectral (VIS-NIR) + RGB; 67,197 annotated pixels | Open | https://telin.ugent.be/~psoubrier/horst/ (code on GitHub) | Hu et al., 2026 |
| YTU-CrackIS (St. Theodore Church, Cappadocia) | Built – rock-hewn church | UAV + terrestrial images, polygon crack annotations, trained weights | Open (PID) | https://doi.org/10.5281/zenodo.19051848 | Kilic et al., 2026 |
| George Town (Penang) weed intrusion | Built – historic urban buildings | 4,522 images / 5,844 bounding boxes | Open (PID) | https://doi.org/10.6084/m9.figshare.29484998 | Chen et al., 2025 |
| REDAI stone deterioration patterns | Built – stone | 354 expert-curated images + code (research use only) | Open | https://github.com/DCorradetti/REDAI_Id_Pattern | Corradetti & Rodrigues, 2025 |
| Historical Building Surface Deterioration Dataset | Built – multi-material (adobe, brick, timber, stone, tile) | 23,688 images, 6 deterioration classes | Open (PID) | https://ieee-dataport.org/documents/historical-building-surface-deterioration-dataset | Bektas Ekici et al., 2026 |
| MSD-Det masonry damage detection | Built – masonry (houses, towers, bridges, Great Wall) | 1,082 high-res images, 8,739 boxes, 7 classes | Open | Google Drive (link in article) | Long et al., 2025 |
| Monastery of Batalha efflorescence | Built – limestone | Images + segmentation masks | Open (PID) | https://doi.org/10.5281/zenodo.21453438 | Bourgeois et al., 2026 |
| Nanjing Ming City Wall defects (CWADE-Net) | Built – brick city wall | 3,206 images (vegetation, spalling) + code | Open | https://github.com/Yuanxlhh/CWADENet | Yuan et al., 2026 |
| Macau gray-brick wall damage | Built – brick | ~1,000-image training set | Open (PID) | https://data.mendeley.com/datasets/rtf5d2v9rm/2 | Yang et al., 2023 |
| Darbhanga Fort damage | Built – brick fort | 643 raw images (7,440 augmented), box + polygon labels | Open (PID) | Mendeley Data (DOI in article) | Singh et al., 2025 |
| Church of São Francisco tile degradation | Built – glazed tiles (azulejos) | 4,965 images, ~33.6k instance labels | Open (PID) | Mendeley Data (link in article) | Karimi et al., 2026 |
| Jiangzhuang Garden crack monitoring | Built – garden architecture | 537 annotated crack images + code | Open | Google Drive (link in article) | Ye et al., 2026 |
| Forbidden City wall brick damage | Built – brick masonry | Sample brick-crop images + code | Partial | https://github.com/DeepDlut/CNN-for-masonry-brick-damage | Wang et al., 2018 |
| Kasbah of Algiers surface damage | Built – historic city | Part of 2,674 cropped images | Partial | Mendeley Data (link in article) | Meklati et al., 2023 |
| Portuguese heritage tiles | Built – glazed tiles | Subset of 5,000+ images | Partial | Mendeley Data (link in article) | Karimi et al., 2024 |
| Multi-material historic-construction cracks | Built – concrete/stone/brick/tile | Subset of images | Partial | Kaggle (link in article) | Karimi et al., 2025 |
| Dadi-Poti tombs damage | Built – stone tombs | Subset of 3,500 images | Partial | Mendeley Data (link in article) | Mishra et al., 2022 |
| Ghent Altarpiece multimodal imagery ("Closer to Van Eyck") | Paintings – panel | Visible, IR, IRR and X-ray macro-imagery | Partial (source imagery only) | http://closertovaneyck.kikirpa.be | Sizyakin et al., 2020 |
| Met Museum + Closer to Van Eyck painting images | Paintings | Public-domain X-ray/visible images; the authors' annotations are not released | Partial (source imagery only) | Metropolitan Museum Open Access; closertovaneyck.kikirpa.be | Mezina et al., 2025 |
| MaDataSet (Bawang Academy timber cracks) | Built – timber | 474 images / 6,608 cracks | Verify | https://github.com/WangMissYou/MaDataSet (the paper's Data Availability statement says "on request") | Ma et al., 2022 |
| Reused public crack/defect benchmarks: BCD, HBC19 (heritage); CCD, BD3 (non-heritage) | Built – brick/stone masonry | Crack image patches | Open | Cited in article | Fallahy & Rezazadeh, 2025 |
| Reused heritage crack datasets: Kaggle "Deterioration Detection in Historical Buildings"; Mendeley "Historical Building Crack 2019" | Built – stone masonry | Crack images | Open | Cited in article | Mayya & Alkayem, 2025 |

#### 1.2 Material characterization

Identifying pigments, fibres, minerals and material properties from spectral, elemental or microscopic data.

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| MA-XRF of two Raphael panel paintings | Paintings – panel | Physics-simulated + real MA-XRF datacubes | Open (PID) | https://zenodo.org/records/12583799 | Preisler et al., 2024 |
| MACLAS Iberian beads | Archaeological objects – personal adornments | Geochemical (XRF) + XRD mineral labels, n≈1,243; code | Open (PID) | https://github.com/Daniel-SanchezG/MACLAS · https://doi.org/10.5281/zenodo.10155331 | Sanchez-Gomez et al., 2024 |
| Layered-pigment XRF mock-ups | Paintings – mock-ups (Gauguin palette) | Simulated + 6,604 real XRF spectra; code | Open | GitHub "deep learning assisted XRF" (link in article) | Xu et al., 2022 |
| Porcelain Relic Microscopic Images (PRMI) | Ceramics – porcelain | Microscopic images, 5 classes | Open | GitHub (link in article) | Liu et al., 2026 |
| Historical PVC plasticizer dataset | Modern materials – plastics | IR spectra + GC-MS for 100+ PVC objects (growing collection) | Open | University of Ljubljana Repository (link in article) | Rijavec et al., 2022 |
| r-FT-IR textile-fibre reference spectra | Textiles | 61 reference textiles, 16 fibre types, >4,000 spectra | Open | Link in article | Peets et al., 2019 |
| Vis-NIR spectra of ancient human ruins | Archaeological sites – soils/features | Spectral images from 27 sites in Central China; code | Verify | GitHub (full URL still to be confirmed) | Luo et al., 2026 |

### Preventive conservation

#### 2.1 Prediction

Forecasting environmental conditions, structural response or deterioration from monitoring data.

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| Archaeological Museum of Delphi, Gallery I microclimate | Museum environment | Hourly indoor T/RH, Aug 2022 – Oct 2024 (+ ERA5-Land reanalysis) | Open | Given in full in the article; ERA5-Land via the Copernicus Climate Data Store | Tringa & Kavroudakis, 2026 |

#### 2.2 Risk assessment

Estimating hazard exposure, vulnerability and risk levels for collections, buildings and sites.

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| Ørholm storage hall & Annisse Church indoor climate | Museum storage / historic church | Hourly indoor/outdoor climate time series + code | Open (PID) | https://doi.org/10.5281/zenodo.6589119 | Boesgaard et al., 2022 |
| Shipwreck loss-mechanism records (Chinese adjacent seas) | Underwater heritage – shipwrecks | Wrecksite.eu records + bathymetry/salinity/ocean-model covariates; code | Open (PID) | https://doi.org/10.5281/zenodo.18046757 | Chen et al., 2026 |
| Aviation Museum Kbely corrosion-risk data | Technical heritage – historic aircraft collection | One year of ambient, pollution and hangar data; trained models | Open (PID) | Zenodo + GitHub (links in article) | Kuchař et al., 2025 |
| Xiwo Qiang Village settlement microclimate | Built – historic settlement | Settlement photographs + field microclimate measurements | Open | Article and Supplementary Information | Lin et al., 2026 |

### Treatment

#### 3.1 Cleaning

No open dataset was identified among the reviewed case studies. Data were either offered only on request or not addressed at all.

#### 3.2 Structural reconstruction

Rejoining fragments and reconstructing the complete form of objects.

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| OBFI oracle-bone fragment images | Archaeological objects – inscribed oracle bones | 5,374 fragment images, 110 expert-confirmed rejoin pairs, 138,855 target-area images; code | Open (PID) | https://doi.org/10.5281/zenodo.10849444 | Zhang et al., 2025 |
| Iberian wheel-made pottery profiles (IberianGAN) | Ceramics – archaeological pottery | 1,075 binary profile images; code | Open | https://github.com/celiacintas/vasijas/tree/iberianGAN | Navarro et al., 2022 |
| Italian Bronze/Iron Age vessel profiles and fragments | Ceramics – archaeological pottery | ~4,000 profile drawings + 417 real fragments; code and notebooks | Open | Supplementary materials of https://doi.org/10.1016/j.culher.2024.09.012 | Cardarelli, 2024 |

#### 3.3 Damage/loss inpainting

Virtual restoration of missing or damaged regions.

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| Jingdezhen export porcelain | Ceramics – porcelain | 2,574 plate images with damage masks | Open (PID) | https://doi.org/10.5281/zenodo.15462784 | Kang & Yang, 2025 |
| Yangshao painted pottery (Miaodigou) | Ceramics – painted pottery | Damaged/original/mask triples + benchmark sets | Open (PID) | https://zenodo.org/records/14026630 | Zhang, 2024 |
| Shaanxi temple murals (LRDiff) | Murals – temple | 351 HD images incl. real damaged murals; data CC-licensed, code Apache-2.0 | Open | https://github.com/CZY-Code/LRDiff | Lei et al., 2025 |
| DhMurals1714 | Murals – Dunhuang cave | 525 real + 1,189 replica murals with line drawings; code | Open | https://github.com/qinnzou/mural-image-inpainting | Li et al., 2024 |
| DMF (Dunhuang Mural Faces) | Murals – Dunhuang cave | 9,552 face images | Open | https://github.com/hqy-hub/DMF-Datsets | Huang et al., 2024 |
| Mural restoration dataset (3,500 images) | Murals | Web-crawled/album-scanned murals, partly from DhMurals1714 | Open | OneDrive (link in the article's Data Availability statement) | Lyu et al., 2025 |
| MaskCLP + MuralVerse (TCSMAF) | Paintings – Chinese scrolls; Murals | 8,273 scrolls with expert-verified real-damage masks + ~8,163 murals; code | Open | https://github.com/LPDLG/TCSMAF | Hu et al., 2026b |
| MuralVerse-S + MaskCLP-S (M3SFormer) | Murals; Paintings – Chinese landscape | ~8,163 murals + 8,273 paintings; masks from real damage; code | Open | https://github.com/LPDLG/M3SFormer | Hu et al., 2026a |
| MaskCLP (Sgrgan) | Paintings – Chinese landscape | 5,621 paintings + masks extracted from real damaged paintings; code | Open | https://github.com/Makbaka1/MaskCLP | Hu et al., 2024b |
| Ancient-painting inpainting dataset | Paintings – Chinese scrolls | Patches from four named masterpieces | Open | https://github.com/luyjsnsndjx/painting-inpainting-dataset | Sun et al., 2024 |
| Synthetic MA-XRF for virtual recolouring (SmallUViT) | Paintings/frescoes – synthetic XRF | ~312,000 synthetic MA-XRF images; code | Open | https://baltig.infn.it/chnet/fast-extended-vision-smalluvit | Bombini et al., 2025 |
| Dunhuang inpainting evaluation outputs | Murals – Dunhuang cave | Damaged test images + inpainted results (base images from the ICCV 2019 e-Heritage Dunhuang challenge) | Open | MDPI supplementary material | Ciortan et al., 2021 |
| Kaggle art-image collections ("Art Images: Drawing/Painting/Sculptures/Engravings"; "Best Artworks of All Time") | General artworks (not heritage-curated) | 2,041 + 1,348 images | Open | Kaggle (URLs in article) | Kumar & Gupta, 2023 |
| SRCLP Chinese-painting dataset | Paintings – Chinese | 900 curated HR paintings | Verify | https://github.com/LPDLG/SRCLP-Dataset (the paper's Data Availability statement says "on request") | Hu et al., 2024a |
| MuralDH-derived Dunhuang restoration data | Murals – Dunhuang cave | Mural, segmentation and super-resolution subsets | Verify | Dryad "share" link in article (not a persistent DOI) | Swathi & Jagannadha Rao, 2026 |

### Documentation

#### 4.1 Point cloud segmentation

| Dataset | Heritage type | Data | Access | Link | Source |
|---|---|---|---|---|---|
| ArCH (Architectural Cultural Heritage) benchmark | Built – churches, cloisters, castles (Italy/Europe) | Annotated TLS/photogrammetric point clouds, 11 scenes (later extended) | Open (research use) | ArCH project site (URL in article, to be confirmed) | Pierdicca et al., 2020 |
| Roman Brick Analysis test set | Built – Roman brick masonry | Small photogrammetric masonry test set + script | Partial | https://github.com/LoreForna/RomanBrickAnalysis | Fornaciari, 2025 |

#### 4.2 Photogrammetry / neural 3D reconstruction

No open heritage dataset was identified among the reviewed case studies. Datasets were self-captured at single sites and not released.

---

## 2. Datasets by heritage type

| Heritage type | Datasets (task) |
|---|---|
| **Built heritage – stone, brick & masonry** | Castle of Horst, YTU-CrackIS, REDAI, Historical Building Surface Deterioration, MSD-Det, Batalha efflorescence, Nanjing Ming City Wall, Macau gray-brick, Darbhanga Fort, Jiangzhuang Garden, Forbidden City brick, Kasbah of Algiers, multi-material cracks, Dadi-Poti tombs, BCD/HBC19, Kaggle/Mendeley heritage-crack sets (condition diagnosis); ArCH, Roman Brick Analysis (point cloud segmentation) |
| **Built heritage – timber** | MaDataSet (condition diagnosis) |
| **Built heritage – glazed tiles** | Church of São Francisco tiles, Portuguese heritage tiles (condition diagnosis) |
| **Built heritage – historic towns & settlements** | George Town weed intrusion (condition diagnosis); Xiwo Qiang Village microclimate (risk assessment) |
| **Paintings (panel, easel, scroll)** | Ghent Altarpiece imagery, Met / Closer to Van Eyck imagery (condition diagnosis); Raphael MA-XRF, layered-pigment XRF mock-ups (material characterization); MaskCLP, MaskCLP-S, ancient-painting inpainting, SRCLP, synthetic MA-XRF (damage/loss inpainting) |
| **Murals & wall paintings** | LRDiff Shaanxi murals, DhMurals1714, DMF, Lyu et al. mural set, MuralVerse / MuralVerse-S, Dunhuang evaluation outputs, MuralDH-derived data (damage/loss inpainting) |
| **Ceramics & pottery** | PRMI porcelain micrographs (material characterization); IberianGAN profiles, Italian Bronze/Iron Age vessels (structural reconstruction); Jingdezhen porcelain, Yangshao painted pottery (damage/loss inpainting) |
| **Other archaeological objects & sites** | MACLAS Iberian beads, Vis-NIR ancient ruins (material characterization); OBFI oracle bones (structural reconstruction) |
| **Textiles** | r-FT-IR textile-fibre spectra (material characterization) |
| **Modern & technical heritage** | Historical PVC objects (material characterization); Aviation Museum Kbely aircraft (risk assessment) |
| **Museum & collection environments** | Delphi Museum microclimate (prediction); Ørholm storage & Annisse Church climate (risk assessment) |
| **Underwater heritage** | Shipwreck loss-mechanism records (risk assessment) |
| **General artworks (not heritage-curated)** | Kaggle art-image collections (damage/loss inpainting) |

---

## 3. Code or results only (no open dataset)

These papers share code, pretrained models or results, but not the underlying heritage data. They are useful for reproducing methods, not as data sources.

| Resource | Task | Link | Source |
|---|---|---|---|
| Adaptive XRF-sampling code (the heritage XRF scan is not shared) | Material characterization | https://github.com/usstdqq/deep-adaptive-sampling-mask | Dai et al., 2020 |
| Ceramic thin-section classification: supplementary results only | Material characterization | https://doi.org/10.5334/jcaa.75.s1 | Lyons, 2021 |
| C3N code + pretrained models (Murals1 dataset only on request) | Damage/loss inpainting | https://github.com/zhangyongqin/C3N | Peng et al., 2023 |
| ArtGAN code (ArtNet dataset not released) | Damage/loss inpainting | https://github.com/namas191297/artgan | Adhikary et al., 2021 |

---

## Source papers

- Adhikary et al. (2021). ArtGAN: Artwork restoration using generative adversarial networks.
- Bektas Ekici et al. (2026). A six-stage ablation-driven benchmarking framework for deep learning-based deterioration classification …
- Boesgaard et al. (2022). Prediction of the indoor climate in cultural heritage buildings through machine learning.
- Bombini et al. (2025). Towards virtual painting recolouring using vision transformer on X-ray fluorescence datacubes.
- Bourgeois et al. (2026). Image-based automatic detection of efflorescence on limestone heritage constructions: Application to the Monastery of Batalha.
- Cardarelli (2024). From fragments to digital wholeness: An AI generative approach to reconstructing archaeological vessels. *Journal of Cultural Heritage*.
- Chen et al. (2025). Weed detection on architectural heritage surfaces in Penang City via YOLOv11.
- Chen et al. (2026). Geospatial predictive modelling of anthropogenic and natural shipwreck risks.
- Ciortan et al. (2021). Colour-balanced edge-guided digital inpainting: Applications on artworks.
- Corradetti & Rodrigues (2025). Identification of stone deterioration patterns with large multimodal models.
- Dai et al. (2020). Adaptive image sampling using deep learning and its application on X-ray fluorescence image reconstruction.
- Fallahy & Rezazadeh (2025). MARBLE-DA: Masonry analysis with robust, batch-normalised, label-free, explainable domain adaptation.
- Fornaciari (2025). AI and deep learning for image-based segmentation of ancient masonry: A digital methodology for mensiochronology of Roman brick.
- Hu et al. (2024a). ConvSRGAN: Super-resolution inpainting of traditional Chinese paintings.
- Hu et al. (2024b). Sgrgan: Sketch-guided restoration for traditional Chinese landscape paintings.
- Hu et al. (2026). Physically interpretable machine learning for facade bio-colonisation.
- Hu et al. (2026a). M3SFormer: Multi-stage semantic and style-fused transformer for mural image inpainting.
- Hu et al. (2026b). TCSMAF: Twin cascade spatial multi-scale attention filtering inpainting of traditional Chinese painting.
- Huang et al. (2024). Enhanced Chinese mural face generation via FreqSplitAttention and dual mask discriminator.
- Kang & Yang (2025). Intelligent restoration expert system design for Jingdezhen export porcelain via improved denoising …
- Karimi et al. (2024). Deep learning-based automated tile defect detection system for Portuguese cultural heritage buildings.
- Karimi et al. (2025). Automated surface crack detection in historical constructions with various materials.
- Karimi et al. (2026). A deep learning-driven mobile application for monitoring of tile degradation in heritage buildings.
- Kilic et al. (2026). Deep learning techniques for crack detection in St. Theodore Church, Cappadocia.
- Kuchař et al. (2025). AI-based decision support system for heritage aircraft corrosion prevention.
- Kumar & Gupta (2023). Restoration of damaged artworks based on a generative adversarial network.
- Lei et al. (2025). Low-rank structure guided diffusion for Shaanxi temple mural restoration.
- Li et al. (2024). Line drawing guided progressive inpainting of mural damage.
- Lin et al. (2026). Optimizing the rapid assessment of microclimate environments in settlement heritage spaces (LLM-enabled framework).
- Liu et al. (2026). InSwAV: Involution enhanced feature clustering and swapped assignments for porcelain relic microscopic image classification.
- Long et al. (2025). MSD-Det: Masonry structures damage detection dataset for preventive conservation of heritage.
- Luo et al. (2026). Enhancing ancient human ruins classification with residual neural networks using visible near-infrared spectra.
- Lyons (2021). Ceramic fabric classification of petrographic thin sections with deep learning.
- Lyu et al. (2025). Mural inpainting via two-stage generative adversarial network.
- Ma et al. (2022). Complex texture contour feature extraction of cracks in timber structures of ancient architecture …
- Mayya & Alkayem (2025). Triple-stage crack detection in stone masonry using YOLO-ensemble, MobileNetV2-U-net, and spectral clustering.
- Meklati et al. (2023). Surface damage identification for heritage site protection: A mobile crowd-sensing solution …
- Mezina et al. (2025). ForgAnoNet: A neural network for anomaly detection in artworks using X-ray and visible spectrum imaging.
- Mishra et al. (2022). Artificial intelligence-based visual inspection system for structural health monitoring of cultural heritage.
- Navarro et al. (2022). Reconstruction of Iberian ceramic potteries using generative adversarial networks.
- Peets et al. (2019). Reflectance FT-IR spectroscopy as a viable option for textile fiber identification.
- Peng et al. (2023). C3N: Content-constrained convolutional network for mural image completion.
- Pierdicca et al. (2020). Point cloud semantic segmentation using a deep learning framework for cultural heritage.
- Preisler et al. (2024). Deep learning for enhanced spectral analysis of MA-XRF datasets of paintings.
- Rijavec et al. (2022). Machine learning-assisted non-destructive plasticizer identification and quantification in historical PVC objects based on IR spectroscopy.
- Sanchez-Gomez et al. (2024). A supervised multiclass framework for mineral classification of Iberian beads.
- Singh et al. (2025). Deep learning-based damage detection and segmentation in the battledore of Darbhanga Fort.
- Sizyakin et al. (2020). Crack detection in paintings using convolutional neural networks.
- Sun et al. (2024). Ancient paintings inpainting based on dual encoders and contextual information.
- Swathi & Jagannadha Rao (2026). Automated image inpainting for historical artifact restoration using hybridisation of transfer learning with deep generative models.
- Tringa & Kavroudakis (2026). Machine learning-based forecasting of indoor microclimate conditions for heritage conservation …
- Wang et al. (2018). Damage classification for masonry historic structures using convolutional neural networks based on still images.
- Xu et al. (2022). Can deep learning assist automatic identification of layered pigments from XRF data?
- Yang et al. (2023). Recognition of damage types of Chinese gray-brick ancient buildings (Macau World Heritage buffer zone).
- Ye et al. (2026). Crack detection and evolution monitoring for heritage buildings: A systematic computer vision-based approach.
- Yuan et al. (2026). CWADE-Net: A deep learning framework for vegetation invasion and brick spalling defect detection on Nanjing Ming City Wall.
- Zhang (2024). AI-assisted restoration of Yangshao painted pottery using LoRA and Stable Diffusion.
- Zhang et al. (2025). Deep rejoining model and dataset of oracle bone fragment images.

---

## Contributing

Know of an open dataset for AI in heritage conservation that is missing here, or found a broken link? Please open an issue or a pull request with the dataset name, heritage type, task, link, and source paper.
