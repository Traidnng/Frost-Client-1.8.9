<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1e3a8a,50:0284c7,100:0f172a&height=220&section=header&text=🧊%20Frost%20Client%201.8.9&fontSize=42&fontColor=ffffff&animation=fadeIn" width="100%"/>

  <p align="center">
    <b>High-Performance • Event-Driven Modular Architecture • Clean Render Engine</b>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Minecraft-1.8.9-2ea44f?style=for-the-badge&logo=minecraft&logoColor=white" alt="Minecraft Version" />
    <img src="https://img.shields.io/badge/Java-8%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
    <img src="https://img.shields.io/badge/Architecture-Event--Driven-blueviolet?style=for-the-badge" alt="Architecture" />
    <img src="https://img.shields.io/badge/MCP-918-0284c7?style=for-the-badge" alt="MCP" />
    <img src="https://img.shields.io/badge/License-MIT-crimson?style=for-the-badge" alt="License" />
  </p>
</div>

---

## 📖 Genel Bakış

**Frost Client**, Minecraft 1.8.9 (MCP 918) tabanı üzerine inşa edilmiş; modüler mimari, düşük gecikmeli olay yönetim sistemi (EventBus) ve optimize edilmiş OpenGL render motoruna sahip özel bir oyun istemcisidir.

> ⚠️ **Yasal Uyarı / Disclaimer:** Bu proje yalnızca tersine mühendislik, istemci mimarisi ve OpenGL render tekniklerini inceleme amacıyla eğitim odaklı geliştirilmiştir.

---

## ⚡ Temel Modüller & Özellikler

### ⚔️ Combat (Savaş Modülleri)
| Modül | Açıklama | Ayarlanabilir Parametreler |
| :--- | :--- | :--- |
| `KillAura` | Önceliklendirilmiş hedef kilitleme & rotasyon motoru | CPS, Range, FOV, Target Priority, Raytrace |
| `Velocity` | Sunucu taraflı geri tepmeyi (knockback) filtreler | Horizontal %, Vertical %, Chance % |
| `AutoClicker` | İnsansı tıklama algoritması ve CPS dalgalanması | Min/Max CPS, Jitter, Right/Left click |
| `AntiBot` | Sahte sunucu botlarını ve NPC'leri filtreler | TabList Check, Ground Check, EntityID |
| `Reach` | Vuruş mesafesini dinamik olarak genişletir | Reach Distance, Sprint Only, Chance |

---

### 🏃 Movement (Hareket Modülleri)
| Modül | Açıklama |
| :--- | :--- |
| `Flight` | Vanilla, Motion ve Glide modlu özel uçuş sistemi |
| `Speed` | Sürtünme ve strafe optimizasyonlu hareket hızlandırma |
| `Sprint` | Her yöne kesintisiz omni-directional otomatik koşu |
| `NoSlow` | Kılıç engelleme, yay çekme ve yemek yeme sırasında hız kaybını önler |
| `Step` | 1-2 blokluk engelleri zıplamadan doğrudan tırmanma |

---

### 👁️ Render & Visuals (Görsel Modüller)
- **2D / 3D ESP:** Kutu, can barı (Health Bar), mesafe ve zırh göstergeleri.
- **Tracers:** Görüş açısındaki varlıklara yönlendirici OpenGL çizgileri.
- **Nametags:** Arkaplan gölgeli, can ve eşya detaylı özel yazı tipleri.
- **Fullbright:** Gece görüşü ve karanlık mağaralar için sabit maksimum gama.
- **Modern HUD & ArrayList:** Aktif modülleri animasyonlu ve renk geçişli listeleme.

---

### ⚙️ Player & World (Oyuncu & Dünya)
- `FastPlace` — Blok koyma gecikmesini sıfırlar.
- `ChestStealer` & `AutoArmor` — Sandık ve zırh yönetim otomasyonu.
- `NoFall` — Düşme paketi (packet) filtreleme.

---

## 🏗️ Mimari & Kod Yapısı
