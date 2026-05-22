<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/not-GIANT/Flame-Unlocker/main/banner.svg">
  <img src="https://raw.githubusercontent.com/not-GIANT/Flame-Unlocker/main/banner.svg" width="100%" alt="Flame Unlocker">
</picture>

<!--BANNER_SVG_START-->
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 320" width="100%">
  <defs>
    <!-- Deep dark background gradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0a0000"/>
      <stop offset="40%" style="stop-color:#1a0500"/>
      <stop offset="100%" style="stop-color:#0d0000"/>
    </linearGradient>

    <!-- Ember glow radial -->
    <radialGradient id="emberGlow" cx="50%" cy="80%" r="55%">
      <stop offset="0%" style="stop-color:#ff4400;stop-opacity:0.35"/>
      <stop offset="60%" style="stop-color:#990000;stop-opacity:0.15"/>
      <stop offset="100%" style="stop-color:#000000;stop-opacity:0"/>
    </radialGradient>

    <!-- Side glow left -->
    <radialGradient id="glowLeft" cx="0%" cy="100%" r="50%">
      <stop offset="0%" style="stop-color:#ff6600;stop-opacity:0.2"/>
      <stop offset="100%" style="stop-color:#000;stop-opacity:0"/>
    </radialGradient>

    <!-- Side glow right -->
    <radialGradient id="glowRight" cx="100%" cy="100%" r="50%">
      <stop offset="0%" style="stop-color:#ff2200;stop-opacity:0.2"/>
      <stop offset="100%" style="stop-color:#000;stop-opacity:0"/>
    </radialGradient>

    <!-- Title text gradient -->
    <linearGradient id="titleGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#ffffff"/>
      <stop offset="30%" style="stop-color:#ffddaa"/>
      <stop offset="70%" style="stop-color:#ff7700"/>
      <stop offset="100%" style="stop-color:#cc2200"/>
    </linearGradient>

    <!-- Subtitle gradient -->
    <linearGradient id="subGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#ff4400;stop-opacity:0"/>
      <stop offset="30%" style="stop-color:#ff8844"/>
      <stop offset="50%" style="stop-color:#ffaa66"/>
      <stop offset="70%" style="stop-color:#ff8844"/>
      <stop offset="100%" style="stop-color:#ff4400;stop-opacity:0"/>
    </linearGradient>

    <!-- Scanline pattern -->
    <pattern id="scanlines" x="0" y="0" width="900" height="4" patternUnits="userSpaceOnUse">
      <rect width="900" height="1" fill="#000" opacity="0.18"/>
    </pattern>

    <!-- Clip for flames -->
    <clipPath id="bannerClip">
      <rect width="900" height="320"/>
    </clipPath>

    <!-- Filter: flame glow blur -->
    <filter id="flameBlur" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="4"/>
    </filter>

    <!-- Filter: text glow -->
    <filter id="textGlow" x="-15%" y="-40%" width="130%" height="180%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="6" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>

    <!-- Filter: ember soft glow -->
    <filter id="emberBlur">
      <feGaussianBlur in="SourceGraphic" stdDeviation="2.5"/>
    </filter>
  </defs>

  <!-- === BACKGROUND === -->
  <rect width="900" height="320" fill="url(#bgGrad)"/>
  <rect width="900" height="320" fill="url(#emberGlow)"/>
  <rect width="900" height="320" fill="url(#glowLeft)"/>
  <rect width="900" height="320" fill="url(#glowRight)"/>

  <!-- Grid lines: horizontal -->
  <g stroke="#ff330018" stroke-width="0.5">
    <line x1="0" y1="40" x2="900" y2="40"/>
    <line x1="0" y1="80" x2="900" y2="80"/>
    <line x1="0" y1="120" x2="900" y2="120"/>
    <line x1="0" y1="160" x2="900" y2="160"/>
    <line x1="0" y1="200" x2="900" y2="200"/>
    <line x1="0" y1="240" x2="900" y2="240"/>
    <line x1="0" y1="280" x2="900" y2="280"/>
  </g>
  <!-- Grid lines: vertical -->
  <g stroke="#ff330010" stroke-width="0.5">
    <line x1="100" y1="0" x2="100" y2="320"/>
    <line x1="200" y1="0" x2="200" y2="320"/>
    <line x1="300" y1="0" x2="300" y2="320"/>
    <line x1="400" y1="0" x2="400" y2="320"/>
    <line x1="500" y1="0" x2="500" y2="320"/>
    <line x1="600" y1="0" x2="600" y2="320"/>
    <line x1="700" y1="0" x2="700" y2="320"/>
    <line x1="800" y1="0" x2="800" y2="320"/>
  </g>

  <!-- === ANIMATED FLAME PARTICLES (background, blurred) === -->
  <g clip-path="url(#bannerClip)" filter="url(#flameBlur)" opacity="0.7">
    <!-- Flame 1 -->
    <ellipse cx="450" cy="290" rx="18" ry="55" fill="#ff6600">
      <animateTransform attributeName="transform" type="translate" values="0,0;-8,-30;4,-55;-5,-80;0,-100" dur="2.2s" repeatCount="indefinite"/>
      <animate attributeName="rx" values="18;12;20;10;16" dur="2.2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.9;0.7;0.85;0.5;0" dur="2.2s" repeatCount="indefinite"/>
    </ellipse>
    <!-- Flame 2 -->
    <ellipse cx="350" cy="300" rx="12" ry="40" fill="#ff4400">
      <animateTransform attributeName="transform" type="translate" values="0,0;5,-20;-4,-45;3,-65;0,-85" dur="1.8s" repeatCount="indefinite" begin="-0.4s"/>
      <animate attributeName="rx" values="12;16;8;14;10" dur="1.8s" repeatCount="indefinite" begin="-0.4s"/>
      <animate attributeName="opacity" values="0.8;0.9;0.65;0.4;0" dur="1.8s" repeatCount="indefinite" begin="-0.4s"/>
    </ellipse>
    <!-- Flame 3 -->
    <ellipse cx="550" cy="295" rx="15" ry="48" fill="#ff8800">
      <animateTransform attributeName="transform" type="translate" values="0,0;6,-25;-6,-50;5,-75;0,-95" dur="2.5s" repeatCount="indefinite" begin="-0.9s"/>
      <animate attributeName="rx" values="15;10;18;12;8" dur="2.5s" repeatCount="indefinite" begin="-0.9s"/>
      <animate attributeName="opacity" values="0.85;0.7;0.9;0.45;0" dur="2.5s" repeatCount="indefinite" begin="-0.9s"/>
    </ellipse>
    <!-- Flame 4 left -->
    <ellipse cx="200" cy="310" rx="10" ry="35" fill="#ff5500">
      <animateTransform attributeName="transform" type="translate" values="0,0;-5,-18;3,-38;-3,-55;0,-72" dur="2.0s" repeatCount="indefinite" begin="-1.1s"/>
      <animate attributeName="opacity" values="0.7;0.6;0.8;0.35;0" dur="2.0s" repeatCount="indefinite" begin="-1.1s"/>
    </ellipse>
    <!-- Flame 5 right -->
    <ellipse cx="700" cy="308" rx="11" ry="38" fill="#ff4400">
      <animateTransform attributeName="transform" type="translate" values="0,0;7,-22;-4,-44;5,-60;0,-80" dur="2.3s" repeatCount="indefinite" begin="-0.6s"/>
      <animate attributeName="opacity" values="0.75;0.65;0.85;0.4;0" dur="2.3s" repeatCount="indefinite" begin="-0.6s"/>
    </ellipse>
  </g>

  <!-- === FLAME CORES (sharp, brighter) === -->
  <g clip-path="url(#bannerClip)" opacity="0.9">
    <ellipse cx="450" cy="295" rx="8" ry="28" fill="#ffcc44">
      <animateTransform attributeName="transform" type="translate" values="0,0;-6,-22;3,-44;-4,-65;0,-82" dur="2.2s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="1;0.8;0.9;0.5;0" dur="2.2s" repeatCount="indefinite"/>
    </ellipse>
    <ellipse cx="350" cy="305" rx="5" ry="18" fill="#ffdd66">
      <animateTransform attributeName="transform" type="translate" values="0,0;4,-15;-3,-32;2,-48;0,-62" dur="1.8s" repeatCount="indefinite" begin="-0.4s"/>
      <animate attributeName="opacity" values="0.9;0.8;0.85;0.4;0" dur="1.8s" repeatCount="indefinite" begin="-0.4s"/>
    </ellipse>
    <ellipse cx="550" cy="300" rx="6" ry="22" fill="#ffbb33">
      <animateTransform attributeName="transform" type="translate" values="0,0;5,-18;-5,-38;4,-58;0,-72" dur="2.5s" repeatCount="indefinite" begin="-0.9s"/>
      <animate attributeName="opacity" values="0.95;0.75;0.9;0.45;0" dur="2.5s" repeatCount="indefinite" begin="-0.9s"/>
    </ellipse>
  </g>

  <!-- === EMBER SPARKS === -->
  <g clip-path="url(#bannerClip)" filter="url(#emberBlur)">
    <circle cx="430" cy="260" r="2.5" fill="#ffaa00">
      <animate attributeName="cy" values="260;200;140;80;20" dur="3s" repeatCount="indefinite"/>
      <animate attributeName="cx" values="430;422;436;418;430" dur="3s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="1;0.8;0.6;0.3;0" dur="3s" repeatCount="indefinite"/>
    </circle>
    <circle cx="465" cy="270" r="2" fill="#ff8800">
      <animate attributeName="cy" values="270;210;155;95;30" dur="2.7s" repeatCount="indefinite" begin="-0.8s"/>
      <animate attributeName="cx" values="465;472;460;475;465" dur="2.7s" repeatCount="indefinite" begin="-0.8s"/>
      <animate attributeName="opacity" values="1;0.9;0.6;0.25;0" dur="2.7s" repeatCount="indefinite" begin="-0.8s"/>
    </circle>
    <circle cx="380" cy="275" r="1.8" fill="#ffcc44">
      <animate attributeName="cy" values="275;215;160;100;40" dur="3.2s" repeatCount="indefinite" begin="-1.5s"/>
      <animate attributeName="cx" values="380;373;385;368;380" dur="3.2s" repeatCount="indefinite" begin="-1.5s"/>
      <animate attributeName="opacity" values="1;0.7;0.5;0.2;0" dur="3.2s" repeatCount="indefinite" begin="-1.5s"/>
    </circle>
    <circle cx="520" cy="265" r="2.2" fill="#ff6600">
      <animate attributeName="cy" values="265;200;145;85;25" dur="2.9s" repeatCount="indefinite" begin="-0.3s"/>
      <animate attributeName="cx" values="520;528;514;530;520" dur="2.9s" repeatCount="indefinite" begin="-0.3s"/>
      <animate attributeName="opacity" values="1;0.85;0.55;0.2;0" dur="2.9s" repeatCount="indefinite" begin="-0.3s"/>
    </circle>
    <circle cx="600" cy="280" r="1.5" fill="#ffaa44">
      <animate attributeName="cy" values="280;225;170;115;55" dur="3.4s" repeatCount="indefinite" begin="-2.1s"/>
      <animate attributeName="opacity" values="0.9;0.7;0.45;0.15;0" dur="3.4s" repeatCount="indefinite" begin="-2.1s"/>
    </circle>
    <circle cx="310" cy="285" r="1.5" fill="#ff7700">
      <animate attributeName="cy" values="285;230;175;120;60" dur="3.1s" repeatCount="indefinite" begin="-1.0s"/>
      <animate attributeName="opacity" values="0.9;0.65;0.4;0.15;0" dur="3.1s" repeatCount="indefinite" begin="-1.0s"/>
    </circle>
  </g>

  <!-- === DECORATIVE SIDE BARS === -->
  <rect x="0" y="0" width="4" height="320" fill="#ff4400" opacity="0.6">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="1.5s" repeatCount="indefinite"/>
  </rect>
  <rect x="896" y="0" width="4" height="320" fill="#ff4400" opacity="0.6">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="1.5s" repeatCount="indefinite"/>
  </rect>

  <!-- Bottom flame bar -->
  <rect x="0" y="306" width="900" height="14" fill="#ff3300" opacity="0.25">
    <animate attributeName="opacity" values="0.25;0.45;0.25" dur="1.8s" repeatCount="indefinite"/>
  </rect>

  <!-- === CORNER ACCENTS === -->
  <!-- Top-left -->
  <polyline points="30,8 8,8 8,30" fill="none" stroke="#ff5500" stroke-width="2" opacity="0.8"/>
  <!-- Top-right -->
  <polyline points="870,8 892,8 892,30" fill="none" stroke="#ff5500" stroke-width="2" opacity="0.8"/>
  <!-- Bottom-left -->
  <polyline points="30,312 8,312 8,290" fill="none" stroke="#ff5500" stroke-width="2" opacity="0.8"/>
  <!-- Bottom-right -->
  <polyline points="870,312 892,312 892,290" fill="none" stroke="#ff5500" stroke-width="2" opacity="0.8"/>

  <!-- === SCANLINES OVERLAY === -->
  <rect width="900" height="320" fill="url(#scanlines)" opacity="0.6"/>

  <!-- === MAIN TITLE === -->
  <!-- Glow layer -->
  <text x="450" y="148" text-anchor="middle" font-family="'Segoe UI', 'Arial Black', sans-serif" font-weight="900" font-size="88" fill="#ff4400" filter="url(#textGlow)" opacity="0.5" letter-spacing="6">FLAME</text>
  <!-- Main text -->
  <text x="450" y="148" text-anchor="middle" font-family="'Segoe UI', 'Arial Black', sans-serif" font-weight="900" font-size="88" fill="url(#titleGrad)" letter-spacing="6">FLAME
    <animate attributeName="opacity" values="1;0.92;1" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- UNLOCKER secondary word -->
  <text x="450" y="200" text-anchor="middle" font-family="'Segoe UI', 'Arial Black', sans-serif" font-weight="900" font-size="42" fill="url(#titleGrad)" letter-spacing="20" opacity="0.95">UNLOCKER</text>

  <!-- === DIVIDER LINE === -->
  <line x1="160" y1="218" x2="740" y2="218" stroke="url(#subGrad)" stroke-width="1.5"/>

  <!-- === TAGLINE === -->
  <text x="450" y="246" text-anchor="middle" font-family="'Courier New', monospace" font-size="13" fill="#ff9966" letter-spacing="5" opacity="0.9">UNLEASH THE BEAST · 144 FPS UNLOCKED</text>

  <!-- === BADGE ROW === -->
  <!-- Badge 1: ROOT -->
  <g transform="translate(198,265)">
    <rect width="100" height="24" rx="4" fill="#3d0000" stroke="#ff3300" stroke-width="0.8"/>
    <text x="50" y="16" text-anchor="middle" font-family="'Courier New', monospace" font-size="10" fill="#ff6644" letter-spacing="1.5">⚡ ROOT</text>
  </g>
  <!-- Badge 2: MAGISK -->
  <g transform="translate(310,265)">
    <rect width="120" height="24" rx="4" fill="#001133" stroke="#3ea6ff" stroke-width="0.8"/>
    <text x="60" y="16" text-anchor="middle" font-family="'Courier New', monospace" font-size="10" fill="#3ea6ff" letter-spacing="1.5">◈ MAGISK</text>
  </g>
  <!-- Badge 3: 144 FPS -->
  <g transform="translate(442,265)">
    <rect width="120" height="24" rx="4" fill="#001a00" stroke="#44ff88" stroke-width="0.8"/>
    <text x="60" y="16" text-anchor="middle" font-family="'Courier New', monospace" font-size="10" fill="#44ff88" letter-spacing="1.5">▲ 144 FPS</text>
  </g>
  <!-- Badge 4: v1.0.0 -->
  <g transform="translate(574,265)">
    <rect width="100" height="24" rx="4" fill="#1a0a00" stroke="#ff9900" stroke-width="0.8"/>
    <text x="50" y="16" text-anchor="middle" font-family="'Courier New', monospace" font-size="10" fill="#ff9900" letter-spacing="1.5">v1.0.0</text>
  </g>

  <!-- === PULSING EMBER AT CENTER BOTTOM === -->
  <circle cx="450" cy="310" r="6" fill="#ff4400" opacity="0.7">
    <animate attributeName="r" values="6;10;6" dur="1.4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.7;0.3;0.7" dur="1.4s" repeatCount="indefinite"/>
  </circle>
  <circle cx="450" cy="310" r="3" fill="#ffcc00" opacity="0.9">
    <animate attributeName="r" values="3;5;3" dur="1.4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.9;0.5;0.9" dur="1.4s" repeatCount="indefinite"/>
  </circle>
</svg>
<!--BANNER_SVG_END-->

[![Root Required](https://img.shields.io/badge/Root-Required-red.svg?style=for-the-badge&logo=android)](https://github.com/not-GIANT/Flame-Unlocker)
[![Magisk](https://img.shields.io/badge/Magisk-Module-3ea6ff.svg?style=for-the-badge&logo=magisk)](https://github.com/topjohnwu/Magisk)
[![FPS](https://img.shields.io/badge/FPS-144%20Unlocked-success.svg?style=for-the-badge&logo=speedtest)](https://github.com/not-GIANT/Flame-Unlocker)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange.svg?style=for-the-badge)](https://github.com/not-GIANT/Flame-Unlocker/releases)

**Break free from software-imposed hardware limits.**

Flame Unlocker is a high-performance system configuration module that redefines your gaming experience. By meticulously spoofing your hardware signature as the **Redmagic 11 Pro (NX809J)**, it bypasses FPS caps and graphical restrictions in top-tier mobile titles.

[**Download Latest Release**](https://github.com/not-GIANT/Flame-Unlocker/releases) • [**Report Issues**](https://github.com/not-GIANT/Flame-Unlocker/issues)

---

</div>

## 🚀 Key Advantages

| Feature | Description |
| :--- | :--- |
| **144 FPS Unlock** | Forces games to recognize high-refresh capabilities, enabling ultra-smooth 144Hz output. |
| **Maximized Graphics** | Unlocks UHD, Extreme, and 90/120/144 FPS options in PUBG, BGMI, CODM, and Genshin. |
| **Elite Identity** | Spoofs the **NX809J** (Redmagic 11 Pro) across all system property levels. |
| **Android 15/16 Ready** | Optimized for modern property management in the latest Android builds. |

---

## 🛠️ Technical Profile

The module targets the following system properties to ensure a seamless "Identity Shift":

```bash
# Redmagic 11 Pro Signature (NX809J)
ro.product.model=NX809J
ro.product.odm.model=NX809J
ro.product.system.model=NX809J
ro.product.vendor.model=NX809J
ro.product.system_ext.model=NX809J
```

---

## 📦 Installation 

### **Prerequisites**
*   **Root Access:** Magisk v24.0+ or equivalent.
*   **High Refresh Rate:** A display capable of 90Hz/120Hz/144Hz (Hardware limitation).

### **Steps to Ignite**
1.  **Obtain:** Download the `flame-unlocker.zip` from the [Releases](https://github.com/not-GIANT/Flame-Unlocker/releases) page.
2.  **Manager:** Open your **Magisk App** and navigate to the `Modules` section.
3.  **Deploy:** Select `Install from Storage` and pick the zip file.
4.  **Verify:** Wait for the custom 🔥 **FLAME UNLOCKER** 🔥 banner to appear in the terminal.
5.  **Finalize:** Reboot your device to apply the new system signature.

---

## 📷 Performance Preview

<div align="center">
  <img src="Screenshot.PNG" width="85%" alt="Performance Preview">
  <p><i>Unlocking peak performance on supported hardware.</i></p>
</div>

---

## ⚠️ Disclaimer & Safety

> [!CAUTION]
> **Performance comes at a cost.** Running games at 144 FPS increases GPU load, power consumption, and thermal output.
> 
> *   This module does **not** overclock hardware; it unlocks software limits.
> *   I am not responsible for hardware fatigue, battery degradation, or account bans.
> *   Always monitor your device temperatures during extended sessions.

---

<div align="center">

### MADE WITH 🔥 BY [GIANT](https://github.com/not-GIANT)

</div>
