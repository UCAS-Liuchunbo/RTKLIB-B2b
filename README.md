# RTKLIB-B2b
An open-source C/C++ toolkit that extends the functionalities of RTKLIB, specifically designed to decode proprietary binary PPP-B2b correction streams and associated navigation messages from prevalent GNSS receivers, and to integrate the decoded corrections for precise point positioning (PPP) using the BeiDou Navigation Satellite System (BDS) PPP-B2b service.

## 🚀 Core Features

### PPP-B2b Decoding
- ​**Receiver Support**
  - ComNav Technology (ComNav) receivers (e.g. K803W)
  - Unicore Communications (Unicore) receivers (e.g. UM980)
  
- ​**Decoded Data**
  - Proprietary binary PPP-B2b correction streams
  - GPS Legacy Navigation (LNAV) messages
  - BDS B1C signal NAV messages (B-CNAV1)
  
- ​**Operation Modes**
  - Real-time decoding
  - Post-processing decoding
  
- ​**Output Format**
  - Extended, BKG Ntrip Client (BNC)-compatible ASCII format

### PPP Positioning
- ​**Positioning Modes**
  - Real-time positioning
  - Post-processing positioning
  
- ​**Satellite Systems**
  - BDS-only mode
  - GPS+BDS combined mode
  
- ​**Positioning Accuracy**
  - Decimeter-level PPP using PPP-B2b corrections

## 🌍 Cross-Platform Support
| Platform       | Real-time | Embedded Platforms  | Recommended Usage            |
|----------------|-----------|---------------------|------------------------------|
| ​**Linux**      | ✔️         | Rk3566, Imx6ull     | Realtime and Post-processing |
| ​**Windows**    | ✔️         | -                   | Post-processing only         |

> 💡 ​**Recommendation**: For best real-time performance, use Unix-like systems (Linux) especially for console-based operations.

## 📊 GNSS Datasets for RTKLIB-B2b

### Complementary Datasets for PPP Research & Validation
This collection supports two key application scenarios: ​**real-time playback simulation** and ​**post-processing analysis** of PPP-B2b corrections. Both datasets are archived on Zenodo:

#### a. Real-time Playback Dataset
**Purpose**: Simulate real-time streams using authentic receiver outputs  
**Equipment**:  
- Receivers: SinoGNSS K803W & Unicore UM980  
- Antenna: CNT AT360  
**Location**: APM Building 1 Rooftop (Wuhan, China)  
**Coverage**:  
- Time: DOY 080-082, 2025 (Mar 21-23, 2025)  
- Data: Raw binary logs (SINO/UNICORE formats)  

🔗 [Download on Zenodo](https://doi.org/10.5281/zenodo.15105929)

#### b. Post-processing Analysis Dataset
**Components**:  
- 1 Hz MGEX observations (gamg, ulab, wuh2)  
- DLR (German Aerospace Center) broadcast ephemeris  
- Unicore PPP-B2b corrections  
**Coverage**:  
- Observations: DOY 065-067, 2025 (Mar 6-8)  
- Ephemeris/Corrections: DOY 065-068, 2025 (Mar 6-9)  

🔗 [Download on Zenodo](https://doi.org/10.5281/zenodo.15110885)

**Usage Recommendations**:  
1. Dataset 1 for testing real-time module via `--playback` mode  
2. Dataset 2 for post-processing validation with precise reference  

## 📄 Citation

If you use RTKLIB-B2b in your research, please cite our paper:

> Liu C, et al. RTKLIB-B2b: Open-source Real-Time Decoding Module for BDS-3 PPP-B2b in RTKLIB. *Measurement Science and Technology*, 2026.  
> DOI: [10.1088/1361-6501/ae58c8](https://doi.org/10.1088/1361-6501/ae58c8)

```bibtex
@article{liu2026rtklib_b2b,
  title={RTKLIB-B2b: Open-source Real-Time Decoding Module for BDS-3 PPP-B2b in RTKLIB},
  author={Liu, Chunbo and others},
  journal={Measurement Science and Technology},
  year={2026},
  doi={10.1088/1361-6501/ae58c8}
}
```

## ❓ Support & Feedback
ℹ️ ​**Detailed description in the [User Manual](manual/RTKLIB-B2b_UserManual.pdf).**  
ℹ️ ​**Developers in China: https://gitee.com/liu-chunbobo/RTKLIB-B2b.git**

## 📜 License

[![GPLv3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Copyright (C) 2024-2026 Chunbo Liu / APM, CAS

This project is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0). You are free to use, modify, and distribute this software under the terms of GPLv3. See the [LICENSE](LICENSE) file for details.