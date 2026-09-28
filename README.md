<!-- ============================== HEADER ============================== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,55:0e7490,100:22d3ee&height=220&section=header&text=Seokmin%20Kang&fontSize=54&fontColor=ffffff&fontAlignY=36&desc=%EA%B0%95%EC%84%9D%EB%AF%BC%20%C2%B7%20Making%20AI%20run%20within%20hardware%20constraints&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="Seokmin Kang banner"/>
</p>

<p align="center">
  <a href="https://github.com/lota09">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2800&pause=900&color=22D3EE&center=true&vCenter=true&width=640&lines=On-device+AI+inference+on+NPUs;INT8+quantization+%C2%B7+HW%2FSW+bit-exact+verification;Computer+architecture+%26+memory+hierarchy;Embedded+firmware+written+from+datasheets" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <code>On-device AI</code> · <code>NPU</code> · <code>Quantization</code> · <code>Computer Architecture</code> · <code>Embedded</code>
</p>

<p align="center">
  <!-- TODO: LinkedIn 주소 입력 -->
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN-ID/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="#-selected-work"><img src="https://img.shields.io/badge/Projects-0E7490?style=for-the-badge&logo=github&logoColor=white" alt="Projects"/></a>
  <a href="#-awards--highlights"><img src="https://img.shields.io/badge/Awards-F59E0B?style=for-the-badge" alt="Awards"/></a>
  <a href="#-tech-stack"><img src="https://img.shields.io/badge/Stack-334155?style=for-the-badge&logo=stackshare&logoColor=white" alt="Stack"/></a>
  <img src="https://komarev.com/ghpvc/?username=lota09&label=VIEWS&color=0e7490&style=for-the-badge" alt="Profile views"/>
</p>

---

### `// about`

Economics student who crossed over into semiconductors — now finishing a **double major in Next-Generation Semiconductor** at Soongsil University.
I like the layer where a model meets real silicon: quantizing it to fit a bit-width, reading the NPU's raw output buffer byte by byte, and finding out which part of the memory hierarchy is actually the bottleneck.

> **A healthy metric is not a healthy system.**
> I once rejected a fire-detection model with 95.31% validation mAP for one with 78.24% — the "better" one kept calling a power-strip LED a fire.

- 🎯 **Focus** — on-device inference · INT8 quantization · HW/SW co-verification · memory-bound workloads
- 🔭 **Now** — YOLOv2 INT8 accelerator for the 2026 Deep Learning HW Design Contest · serving LLMs on a mining GPU (CMP 170HX)
- 🌱 **Growing into** — NPU runtime / system software, FPGA·ASIC architectures that care about area and power
- 🤝 **Open to** — NPU SW · system SW · architecture & performance analysis roles

---

### 🏆 Awards & Highlights

<table>
  <tr>
    <td align="center" width="25%">
      <h3>🥇</h3>
      <b>Grand Prize</b><br/>
      <sub>2026 Project Report Challenge (CPC)<br/>Parallel MJPEG converter · 1st of 12 teams</sub>
    </td>
    <td align="center" width="25%">
      <h3>🏅</h3>
      <b>COSS Council Chair Award</b><br/>
      <sub>2025 WE-Meet Project · Jan 2026<br/>Next-Gen Semiconductor consortium</sub>
    </td>
    <td align="center" width="25%">
      <h3>🎙️</h3>
      <b>Oral Presentation</b><br/>
      <sub>ICOS 2026 · Da Nang, Vietnam<br/>SPEC2000 performance analysis (in English)</sub>
    </td>
    <td align="center" width="25%">
      <h3>🎓</h3>
      <b>2 Microdegrees</b><br/>
      <sub>Next-Gen Semiconductor System·SW<br/>Intermediate + Advanced</sub>
    </td>
  </tr>
</table>

---

### 🛠 Selected Work

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>⚡ YOLOv2 INT8 Quantization & MAC Accelerator</h4>
      <sub><code>2026.01 – now</code> · 2026 Deep Learning HW Design Contest</sub>
      <ul>
        <li>Raised INT8 mAP <b>54.91% → 79.28%</b> (+24.37%p, FP32 81.76%)</li>
        <li>Found the <b>“Bias Wall”</b>: every layer in the clipping golden zone, yet mAP collapsed to 1.97% — bias scale overflowed INT16</li>
        <li>16-lane MAC + 4-stage adder tree (<b>9-cycle</b> pipeline), DSP48 / LUT fallback</li>
        <li>Pixel-level HW↔SW bit-exact cross-check pipeline</li>
      </ul>
      <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/> <img src="https://img.shields.io/badge/Verilog-0E7490?style=flat-square"/> <img src="https://img.shields.io/badge/Vivado-ED1C24?style=flat-square&logo=amd&logoColor=white"/><br/>
      <a href="https://github.com/lota09/AIX2026">→ repo</a>
    </td>
    <td width="50%" valign="top">
      <h4>🧵 Parallel MJPEG Converter <sup>🥇 CPC Grand Prize</sup></h4>
      <sub><code>2026.03 – 2026.06</code> · Operating Systems team project</sub>
      <ul>
        <li>fork + thread pipeline with bounded buffers: up to <b>3.45×</b> over sequential</li>
        <li>Designed the sync experiments: no lock → <b>80.71%</b> lost updates; semaphore <b>4.96×</b> slower than mutex; atomic 21% faster</li>
        <li>Same fps (1.002×) but <b>1.7×</b> CPU time for spin vs cond_var</li>
        <li>Amdahl limit on 1–8 cores (8-core efficiency 47.3%)</li>
      </ul>
      <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/> <img src="https://img.shields.io/badge/pthreads-334155?style=flat-square"/> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black"/> <img src="https://img.shields.io/badge/gem5-0F172A?style=flat-square"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🏠 On-device AI Home Safety on DeepX NPU</h4>
      <sub><code>2025.11 – 2025.12</code> · NPU-based AI Inference (A+, 100/100)</sub>
      <ul>
        <li>Parsed the NPU's <b>256-byte raw pose buffer</b> by offset → 17 keypoints</li>
        <li>Fire, fall, intrusion and sleep monitoring fully on-device (Orange Pi 5 Plus)</li>
        <li>Chose the <b>78.24%</b> model over the 95.31% one after testing on unseen real video</li>
        <li>Presence check: ARP + OS table + ping sweep, ~30% → <b>95%+</b></li>
      </ul>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white"/> <img src="https://img.shields.io/badge/DeepX_NPU-0F172A?style=flat-square"/><br/>
      <a href="https://github.com/lota09/NPU_25_2">→ repo</a>
    </td>
    <td width="50%" valign="top">
      <h4>🧮 SPEC2000 Design-Space Exploration</h4>
      <sub><code>2025.09 – 2025.12</code> · Computer Architecture · presented at ICOS 2026</sub>
      <ul>
        <li><b>1,620</b> processor/cache configs × 4 benchmarks on SimpleScalar</li>
        <li>mcf: L2 512 KB → 2 MB gave <b>IPC +20.0%</b>, L2 miss 25.66% → 12.56%</li>
        <li>Branch prediction, not issue width, dominates the memory-bound mcf</li>
        <li>Automated config generation, runs and analysis</li>
      </ul>
      <img src="https://img.shields.io/badge/SimpleScalar-334155?style=flat-square"/> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white"/><br/>
      <a href="https://github.com/lota09/CA_25_2">→ repo</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🌬️ AutoExhaust — 3D Printer MQTT Controller</h4>
      <sub><code>2026.02 – now</code> · personal</sub>
      <ul>
        <li>Subscribes to Bambu Lab X1C over <b>MQTTS (TLS, 8883)</b>, filters a 20 KB JSON stream</li>
        <li>6-state FSM, non-blocking loop, ESP32 light-sleep</li>
        <li>Measured LED load at <b>133%</b> of PSU rating; root-caused a dead board to MOSFET gate breakdown</li>
      </ul>
      <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white"/> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/><br/>
      <a href="https://github.com/lota09/AutoExhaust">→ repo</a>
    </td>
    <td width="50%" valign="top">
      <h4>👁️ Sauron — Notice Crawler & Discord Bot</h4>
      <sub><code>2024.11 – now</code> · in production</sub>
      <ul>
        <li>Crawls department notices, summarizes with AI, pushes to Discord</li>
        <li><b>21 months</b> of maintenance, 80+ commits, rotating logs</li>
        <li>Console + daily rotating file logs for unattended operation</li>
      </ul>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white"/> <img src="https://img.shields.io/badge/Discord-5865F2?style=flat-square&logo=discord&logoColor=white"/><br/>
      <a href="https://github.com/lota09/sauron">→ repo</a>
    </td>
  </tr>
</table>

<details>
  <summary><b>📂 More projects (15)</b></summary>
  <br/>

| Area | Project | What it does |
| :-- | :-- | :-- |
| 🤖 AI / LLM | [vllm](https://github.com/lota09/vllm) | vLLM serving on an NVIDIA CMP 170HX mining GPU, with setup scripts and benchmarks |
| 🤖 AI / LLM | [local_LLM_llama](https://github.com/lota09/local_LLM_llama) | Local LLM runtime setup |
| 🤖 AI / LLM | [auto-typesetter](https://github.com/lota09/auto-typesetter) | Detects speech bubbles and speakers, translates and re-typesets comics into Korean |
| 🤖 AI / LLM | [ICT-project](https://github.com/lota09/ICT-project) | LLM + OCR academic-notice alert system |
| 🤖 AI / LLM | [AI_System_25_W](https://github.com/lota09/AI_System_25_W) | Real-time ASL digit hand-pose recognition |
| 🔩 Hardware | [Project_FIR_DSD_25_2](https://github.com/lota09/Project_FIR_DSD_25_2) | 33-tap reconfigurable FIR filter and control FSM |
| 🔩 Hardware | [Digital-Logic-Circuit](https://github.com/lota09/Digital-Logic-Circuit) | Digital logic designs in Verilog |
| 🔩 Hardware | [microprocessor-25-1](https://github.com/lota09/microprocessor-25-1) | Microprocessor applications in assembly |
| 📟 Embedded | [Embedded_25_W](https://github.com/lota09/Embedded_25_W) | STM32 / AVR drivers (SPI OLED, WS2812, encoder) + Hangman game |
| 📟 Embedded | [Trainsmit](https://github.com/lota09/Trainsmit) | ESP32 transit-arrival display using Seoul open data |
| ⚙️ Automation | [Commute](https://github.com/lota09/Commute) | Termux commute log with automatic pay calculation |
| ⚙️ Automation | [Smarttings-Collections](https://github.com/lota09/Smarttings-Collections) | SmartThings automation scripts |
| 🧠 ML | Colored MNIST | HOG + XGBoost 98.34%; reported a −0.22% augmentation result honestly |
| 🌐 Open source | [DroidDesk](https://github.com/lota09/DroidDesk) | Upstream fix merged: rooted chroot mount check + env leak |
| 🧩 Algorithms | [algorithm-25-1](https://github.com/lota09/algorithm-25-1) | Data structures & algorithms coursework |

</details>

---

### 🧰 Tech Stack

**Languages**<br/>
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/>
<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Verilog_HDL-0E7490?style=flat-square"/>
<img src="https://img.shields.io/badge/Assembly-6E4C13?style=flat-square"/>
<img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white"/>
<img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-003B57?style=flat-square&logo=sqlite&logoColor=white"/>

**AI · Inference**<br/>
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
<img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white"/>
<img src="https://img.shields.io/badge/DeepX_DXNN-0F172A?style=flat-square"/>
<img src="https://img.shields.io/badge/FuriosaAI_NPU-0F172A?style=flat-square"/>
<img src="https://img.shields.io/badge/YOLO-00FFFF?style=flat-square&logoColor=black"/>
<img src="https://img.shields.io/badge/vLLM-30A2FF?style=flat-square"/>
<img src="https://img.shields.io/badge/llama.cpp-000000?style=flat-square"/>
<img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white"/>
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/XGBoost-189C5A?style=flat-square"/>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>

**Hardware · Architecture**<br/>
<img src="https://img.shields.io/badge/Vivado-ED1C24?style=flat-square&logo=amd&logoColor=white"/>
<img src="https://img.shields.io/badge/Vitis-ED1C24?style=flat-square&logo=amd&logoColor=white"/>
<img src="https://img.shields.io/badge/Zynq_FPGA-ED1C24?style=flat-square&logo=amd&logoColor=white"/>
<img src="https://img.shields.io/badge/AXI4--Lite-334155?style=flat-square"/>
<img src="https://img.shields.io/badge/SimpleScalar-334155?style=flat-square"/>
<img src="https://img.shields.io/badge/gem5-334155?style=flat-square"/>
<img src="https://img.shields.io/badge/Keil_MDK-0091BD?style=flat-square&logo=arm&logoColor=white"/>

**Embedded · IoT**<br/>
<img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white"/>
<img src="https://img.shields.io/badge/AVR-EC1B24?style=flat-square&logo=microchip&logoColor=white"/>
<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white"/>
<img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white"/>
<img src="https://img.shields.io/badge/Orange_Pi-FF6600?style=flat-square"/>
<img src="https://img.shields.io/badge/FreeRTOS-5DB136?style=flat-square"/>
<img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white"/>
<img src="https://img.shields.io/badge/Home_Assistant-18BCF2?style=flat-square&logo=homeassistant&logoColor=white"/>

**Systems · Tools**<br/>
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white"/>
<img src="https://img.shields.io/badge/Android_chroot-3DDC84?style=flat-square&logo=android&logoColor=white"/>
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white"/>
<img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white"/>
<img src="https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white"/>

---

### 📜 Education & Training

<table>
  <tr><th align="left">When</th><th align="left">What</th></tr>
  <tr><td><code>2020.03 – 2027.02 (exp.)</code></td><td><b>Soongsil University</b> — B.A. Economics · <b>Double major: Next-Generation Semiconductor</b> (43 credits)<br/><sub>A+: NPU-based AI Inference (100), Digital System Design, Digital Logic Circuits, Data Structures & Algorithms, AI System Design Project</sub></td></tr>
  <tr><td><code>2026.02</code></td><td>Microdegree — Next-Gen Semiconductor <b>System·SW, Advanced</b></td></tr>
  <tr><td><code>2025.12</code></td><td>mySUNI × SK hynix badges — <b>DRAM Operation Lv.2</b>, <b>NAND Operation Lv.2</b>, DRAM Characteristics Lv.1, Semiconductor Market Lv.1</td></tr>
  <tr><td><code>2025.08</code></td><td>Microdegree — Next-Gen Semiconductor <b>System·SW, Intermediate</b></td></tr>
</table>

<details>
  <summary><b>🏅 All awards & activities (7)</b></summary>
  <br/>

| When | Award / Activity | Note |
| :-- | :-- | :-- |
| 2026.07 | 🥇 **Grand Prize**, 2026 Project Report Challenge (CPC) | Parallel MJPEG converter on multi-core · ceremony 2026.10 |
| 2026.01 | 🎙️ **Oral presentation**, ICOS 2026 (Da Nang) | “A Simulation-Based Performance Analysis of SPEC2000 Benchmarks” |
| 2026.01 | 🏅 **COSS Council Chair Award**, 2025 WE-Meet Project | Next-Gen Semiconductor consortium |
| 2025.10 | SEDEX 2025 Semiconductor Exhibition | Visit |
| 2025.09 | 🥈 **Excellence Award**, 2025 Project Report Challenge (CPC) | ARM code optimization for image converting (Keil MDK) |
| 2023.01 | AICE BASIC (KT) | AI / statistical analysis certificate |
| 2022 | Codeground SCPC 2022 (Samsung) | Participant |

</details>

<details>
  <summary><b>📚 Semiconductor short courses (8 · 145 h)</b></summary>
  <br/>

| When | Course | Hours |
| :-- | :-- | --: |
| 2026.02 | SoC & FPGA SW/HW mixed-block design (Advanced) | 20 |
| 2025.08 | Memory semiconductor fundamentals | 15 |
| 2025.08 | SoC chip power & die-size estimation | 24 |
| 2025.07 | Computer vision on NPU with FuriosaAI | 8 |
| 2025.07 | Introduction to TCAD | 12 |
| 2025.01 | Digital logic design on FPGA | 20 |
| 2024.07 | SoC & HW IP design lab | 16 |
| 2024.01 | Embedded SW with Arduino | 30 |

</details>

---

### 📈 GitHub Activity

<!--
  github-readme-stats 공개 서버(github-readme-stats.vercel.app)는 2026-09 현재 일시중지 상태.
  직접 Vercel에 배포(self-host)한 뒤 아래 주석을 풀고 도메인만 바꾸면 통계·언어 카드가 추가된다.
<p align="center">
  <img height="165" src="https://YOUR-STATS.vercel.app/api?username=lota09&show_icons=true&count_private=true&hide_border=true&bg_color=00000000&title_color=22d3ee&icon_color=22d3ee&text_color=8b949e&ring_color=0e7490" alt="GitHub stats"/>
  <img height="165" src="https://YOUR-STATS.vercel.app/api/top-langs/?username=lota09&layout=compact&langs_count=8&hide_border=true&bg_color=00000000&title_color=22d3ee&text_color=8b949e" alt="Top languages"/>
</p>
-->

<p align="center">
  <img src="https://streak-stats.demolab.com?user=lota09&hide_border=true&background=00000000&ring=22D3EE&fire=0E7490&currStreakLabel=22D3EE&sideLabels=8B949E&currStreakNum=8B949E&sideNums=8B949E&dates=8B949E" alt="Streak"/>
</p>

<!-- 3D 잔디: .github/workflows/profile-3d.yml 이 매일 생성 -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./profile-3d-contrib/profile-night-rainbow.svg"/>
    <img src="./profile-3d-contrib/profile-gitblue.svg" alt="3D contribution graph" width="100%"/>
  </picture>
</p>

---

<p align="center"><sub>Measure · Doubt the metric · Verify</sub></p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:22d3ee,45:0e7490,100:0f172a&height=110&section=footer" width="100%" alt="footer"/>
</p>
