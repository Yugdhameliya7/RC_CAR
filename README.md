# ESP32 Bluetooth Controlled RC Car 🚗

An ESP32-based Bluetooth-controlled RC car built using the L298N motor driver. The car can be wirelessly controlled from an Android device over Bluetooth and includes features such as adjustable speed, horn control, and connection status indication.

## Features

* 📱 Bluetooth control using the ESP32's built-in Bluetooth
* ⬆️ Forward, backward, left, right, and stop movement
* ⚡ Boost mode for increased motor speed
* 🔊 Toggleable horn (buzzer)
* 💡 LED connection indicator

  * Solid ON when a Bluetooth device is connected
  * Blinking when waiting for a connection
* 🎮 Simple single-character command interface for easy integration with custom Android apps or Bluetooth terminal applications

## Hardware Used

* ESP32 Development Board
* L298N Motor Driver
* 4 DC Gear Motors
* Chassis with wheels
* Active Buzzer
* LED
* Battery Pack
* Jumper Wires

## Pin Configuration

| Component | ESP32 Pin |
| --------- | --------: |
| ENA       |    GPIO 2 |
| ENB       |    GPIO 4 |
| IN1       |   GPIO 18 |
| IN2       |   GPIO 19 |
| IN3       |   GPIO 22 |
| IN4       |   GPIO 23 |
| Buzzer    |    GPIO 5 |
| LED       |   GPIO 21 |

## Bluetooth Commands

| Command | Action            |
| ------- | ----------------- |
| F       | Move Forward      |
| B       | Move Backward     |
| L       | Turn Left         |
| R       | Turn Right        |
| S       | Stop              |
| Y       | Toggle Horn       |
| Z       | Toggle Boost Mode |

## Working

After powering on, the ESP32 creates a Bluetooth device named **ESP32_CAR**. Once connected, the onboard status LED remains ON. Commands sent from a Bluetooth application control the motors in real time. Boost mode increases motor speed, while the horn can be toggled independently without affecting movement.

## Future Improvements

* Obstacle avoidance using an ultrasonic sensor
* Servo-based environment scanning
* Speed control using PWM (LEDC)
* Mobile app with joystick controls
* Battery voltage monitoring
* Autonomous navigation mode

## License

This project is open-source and intended for educational and learning purposes.
