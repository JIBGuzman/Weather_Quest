# Embedded Weather Quester Project

## Overview
The Embedded Weather Quester is an advanced IoT application integrating the TM4C123 LaunchPad with a CC3100 Booster Pack and ST7735 Color LCD. The system fetches weather information from an online API and displays it with animations, multiple fonts, and colors. It also provides a UART PC serial terminal interface for interactive queries.

## Features
- Display weather information for multiple cities (New York, London, Seattle).
- Supports querying by city name, city ID, geographic coordinates, and zip code.
- Animations for weather conditions: sunny, cloudy, rainy.
- Temperature data display including current, minimum, and maximum in Fahrenheit.
- Humidity and weather condition icons shown on ST7735 LCD.
- User interaction via onboard switches and UART serial input.
- Background color changes and different font sizes for readability.
- Real-time updates triggered by user input or switch presses.
- Uses interrupts and SysTick timer for animations and smooth display updates.

## Hardware Components
- TM4C123 LaunchPad microcontroller
- CC3100 Booster Pack for WiFi connectivity
- ST7735 128x160 Color LCD
- UART interface for serial communication
- Onboard switches for user input
- Power supplied via USB connection

## Software Design
- Secure HTTP communication using the CC3100 WiFi module to fetch weather data from OpenWeatherMap API.
- Parsing JSON-like responses to extract relevant weather information.
- State machine to manage query inputs and display updates.
- Efficient graphics programming for LCD including text rendering, background fills, and animations.
- Interrupt-driven design using SysTick timer to handle animations and display refresh.
- UART input handling for user query criteria and control commands.
- Modular design separating LCD control, WiFi communication, data parsing, and user interface logic.

## Usage Instructions
1. Power the LaunchPad and connect the CC3100 Booster Pack and ST7735 LCD.
2. Use onboard switches to cycle through weather scenarios or enter query mode.
3. Enter queries via UART serial terminal for city name, city ID, coordinates, or zip code.
4. Weather data updates on the LCD with appropriate icons and animations.
5. Repeat or change queries to view new weather information.

## Challenges and Learnings
- Integrating multiple hardware components over I2C, SPI, UART, and WiFi.
- Ensuring stable WiFi connectivity with CC3100 Booster Pack.
- Parsing complex API responses accurately within microcontroller constraints.
- Developing smooth and visually appealing LCD animations with limited resources.
- Managing interrupt-driven updates alongside blocking network operations.
- Troubleshooting hardware connection issues and refining user interface interaction.

## Contributors
- Jonathan Cerniaz
- Joseph Guzman
- Afzal Hakim
- Robby Rimal
