# STM32G491RE with Waveshare 2.4-inch LCD Module 📺

Welcome to the STM32G491RE project, where we interface with the Waveshare 2.4-inch LCD Module using SPI! 🎉

## Project Overview 🚀

In this project, we've set up the STM32G491RE to communicate with the Waveshare 2.4-inch LCD Module via SPI1. This allows us to display data on the LCD screen at high speed while keeping everything synchronized with the microcontroller's capabilities. Let's dive into the details!

## SPI Configuration 🛠️

We are using **SPI1** in the following configuration:

- **Data Length:** 8-bit Motorola 🛠️
- **SPI Clock Frequency:** The STM32G491RE Nucleo board operates at a clock frequency of 170 MHz. However, the maximum supported SPI speed for the LCD controller is 75 Mbit/sec.
- **SPI Prescaler:** To ensure compatibility, we've set the SPI Prescaler to **8**. This gives us an SPI clock speed of **21.25 Mbit/sec** (170 MHz / 8). ⚡

### Why Prescaler 8? 🤔

The LCD controller doesn't support speeds higher than 21.25 Mbit/sec. While using a Prescaler of **4** would theoretically double the SPI speed, it exceeds the LCD controller's maximum supported speed and would result in malfunction. 🚫

## Timer Configuration for PWM 🕒

- **Timer Used:** `TIM3`
- **Channel Used:** `CH2`
- **PWM Generation:** We've utilized **Channel 2 (CH2)** of TIM3 for generating PWM signals to drive the LCD module. This ensures precise timing and control over the display. ⏱️

## Getting Started 🏁

1. **Clone this repository** to your local environment.
2. **Open the project** in your preferred STM32 IDE.
3. **Compile and upload** the code to your STM32G491RE Nucleo board.
4. **Connect the Waveshare 2.4-inch LCD Module** to the appropriate pins on the STM32G491RE.
5. **Power on** your setup and watch the magic happen on the LCD! 🌟

## Conclusion 🎉

This setup allows for a smooth and efficient interface with the Waveshare 2.4-inch LCD Module using SPI at 21.25 Mbit/sec. The timing and speed configurations ensure that the LCD operates within its specifications, providing a reliable and high-quality display experience.
