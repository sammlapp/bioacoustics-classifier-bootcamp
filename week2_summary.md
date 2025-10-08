# Lecture Outline: Sound, Digital Audio, and Annotation

---

## 🕐 13:51–13:58 — Introduction
- Setup and greetings.  
- Overview of session: **sound, digital audio, waveforms, preprocessing**.  
- Will also work with participants’ own recordings / focal species.  
- Quick check-in on any issues from prior work.  

---

## 🕐 13:58–14:04 — What Is Sound?
- **Sound = perception** of an **acoustic signal**.  
- **Acoustic signal** = longitudinal pressure wave (compression & rarefaction of air or water).  
- Sound waves travel through **matter**, not light waves.  
- Analogy: moves like a **slinky**, not like ocean waves.  
- Can exist in solids but behaves differently (surface & transverse components).  

---

## 🕐 14:04–14:07 — Point Sources & Energy Loss
- Sound radiates spherically from a source.  
- Intensity decreases with **distance² (1/r² law)** because energy spreads over a larger sphere.  
- Discussion of “tree falls in forest” — distinction between acoustic wave and heard sound.  

---

## 🕐 14:07–14:10 — From Sound to Digital Audio
- Microphone = membrane that moves with pressure.  
- Pressure → voltage → sampled numbers.  
- **Sample rate** = number of pressure readings per second (e.g. 32 kHz = 32,000 samples/s).  
- **WAV file** = uncompressed list of amplitude samples.  
- Other formats (MP3, FLAC) are compressed or encoded differently.  

---

## 🕐 14:10–14:15 — Sound Propagation, Echo, Reverberation
- **Speed of sound** ≈ 330 m/s (air) ≈ 1000 m/s (water).  
- Light ≈ 3 × 10⁸ m/s → sound is *very slow* in comparison.  
- **Echo** = distinct reflection after a delay.  
- **Reverberation** = dense, short-delay reflections that smear energy in time (visible in spectrograms).  

---

## 🕐 14:15–14:21 — Physical Properties of Waves
- **Amplitude → loudness**.  
- **Frequency → pitch** (Hz = cycles per second).  
- **Phase** rarely perceptible.  
- **Pitch perception is logarithmic** → doubling frequency = one octave higher.  
  - e.g. 100 Hz → 200 Hz → 400 Hz → 800 Hz = successive octaves.  

---

## 🕐 14:21–14:26 — Viewing Audio in Audacity
- Stereo = two microphones (two similar waveforms).  
- Values scaled to **–1 → +1** amplitude range.  
- **Gain** controls how much pressure corresponds to digital amplitude.  
- **Bit depth** = number of bits per sample → resolution of amplitude:
  - 16-bit → 65,536 levels; 32-bit → very high resolution.  
- **Clipping** occurs when signal exceeds ±1 → distortion / “crunchy” sound.  

---

## 🕐 14:26–14:33 — Spectrograms & Source Separation
- A single waveform is a **mixture of all sound sources**.  
- Human ear separates frequencies via **cochlea** → similar to spectrogram math.  
- **Spectrogram = time × frequency × amplitude** image.  
  - Computed using **short-time Fourier transform (STFT)** over sliding windows.  
- **Window-size trade-off:**
  - Long window → good frequency resolution, poor time resolution.  
  - Short window → good time resolution, poor frequency resolution.  
- Typical compromise for bird/frog calls: ~512-sample window at 32 kHz.  

---

## 🕐 14:33–14:42 — Data Annotation for ML
- Transition to **machine-learning preparation**.  
- Need labeled data (positive/negative, species presence).  
- **Weak label** = species known to occur somewhere in clip.  
- **Strong label** = exact time/frequency bounds.  
- Handle clips with multiple species → **multi-class labeling (0/1 per class)**.  
- Annotation tools: **Raven**, **Audacity** (boxes + labels).  
- Projects discussed:
  - Bird begging calls (≈ 21 clips, 120 vocalizations).  
  - Frog call dataset (6 species, 500–1800 clips each).  
  - Hawaiian birds, multi-class annotations, field vs. repository data.  

---

## 🕐 14:42–14:48 — Fourier Transform & Spectrogram Math
- Spectrogram = sequence of frequency spectra over time.  
- **Fourier Transform** converts time-domain waveform → frequency-domain amplitudes.  
- Conceptually: sum of **sine waves** with different amplitudes & phases.  
- **Amplitude** = energy at frequency; **phase** = starting offset.  
- Spectrograms usually **discard phase**, keep amplitude only.  
- Recommended reading: *Brian McFee – Digital Audio Signal Processing* (open textbook).  

---

## 🕐 14:48–14:49 — Wrap-Up
- Plan for next week: continue coding and model development.  
- Instructor stops recording after screen-sharing issue noted.  

---

## ✅ Key Takeaways
- Sound = pressure variation → recorded as sampled numbers.  
- Sample rate & bit depth control digital precision.  
- Spectrograms visualize frequency content; window length = time/frequency trade-off.  
- Annotation quality (weak vs. strong labels) crucial for training classifiers.  
- Fourier Transform is the core mathematical bridge between waveform and frequency analysis.  
