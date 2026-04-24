# Smart Fan

---

**Smart Fan** adalah proyek berbasis Arduino Uno R3 yang mensimulasikan kipas pintar. Sistem ini menggunakan motor DC sebagai kipas, servo sebagai penggerak arah angin (wiper style), potensiometer untuk mengatur kecepatan, tombol ON/OFF untuk kontrol, LED sebagai indikator, dan LCD I2C untuk menampilkan status sistem secara real-time.

---

## Pin Configuration

| Component          | Arduino Pin | Description                  | Power Connection |
| :----------------- | :---------: | :--------------------------- | :--------------- |
| **LCD 16x2 I2C**   | SDA=A4, SCL=A5 | Status Monitoring          | 5V & GND |
| **Potentiometer**  | A0          | Speed Control (PWM input)    | 5V & GND |
| **Push Button ON** | D4          | Motor ON (Input Pull-up)     | GND |
| **Push Button OFF**| D5          | Motor OFF (Input Pull-up)    | GND |
| **Motor DC**       | D10 (PWM)   | Fan Motor Control            | External VCC & GND |
| **Servo Motor**    | D9          | Fan Direction (Wiper style)  | 5V & GND |
| **LED Indicator**  | D2          | Motor Status Indicator       | 5V & GND |

---

## Operational Workflow

1. **Startup:** Sistem standby dengan LCD menampilkan “Motor OFF”.
2. **ON Button:** Tekan tombol ON → servo aktif, LED menyala, LCD menampilkan kecepatan motor.
3. **Speed Control:** Potensiometer mengatur kecepatan motor (PWM 0–255).
4. **Servo Movement:** Servo bergerak bolak‑balik 0–180° seperti kipas angin, berhenti di posisi terakhir saat OFF.
5. **OFF Button:** Tekan tombol OFF → motor masih nyala, servo mati, LED padam, LCD menampilkan “Motor OFF”.

---

## Project Documentation
* **Source Code:** [Code.ino](https://github.com/RizkiFachrudin/UTS_MIKROKONTROLLER_ACHMAD-RIZKI-F/blob/main/KODE%20UTS%20MIKROKONTROL)
* **Circuit Schematic:** [Wiring Diagram](https://github.com/RizkiFachrudin/UTS_MIKROKONTROLLER_ACHMAD-RIZKI-F/blob/main/SKEMA%203D%20UTS%20MIKROKONTROLER.png)
* **Simulation Video:** [Demo Video](https://github.com/RizkiFachrudin/UTS_MIKROKONTROLLER_ACHMAD-RIZKI-F/blob/main/VIDEO%20PRAKTEK%20UTS%20MIKROKONTROL.mp4)
* **Cirkit Designer IDE:** [Try Simulation](https://app.cirkitdesigner.com/project/01d0b176-fb64-4b72-b61e-f3bd2cb71a0e)

---
*Developed by [Achmad Rizki Fachrudin](https://github.com/RizkiFachrudin)*
