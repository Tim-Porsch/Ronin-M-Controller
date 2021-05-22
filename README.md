# Ronin-M-Controller

## This is my 1st project on GitHub
- so please be kind to me. I have some experience with MCU's because I did my "Facharbeit" which is like a paper we have to create in high school here in Germany about that topic.
- Also be aware that the English language is not my native tongue, and I'm still learning it in school

## the goals of the project
- I own a DJI Ronin M which I used to stabilize my camera while filming. It's great, but I miss the feature of controlling where the camera is pointing to. The result of the project should be a thumb controller like the commercial one from DJI but for me, that variant is way too expensive. Also, I want to create a follow focus System for it, but this is going to be another project of mine later on.
---
## realization of the goals
**quick schematica**
![1](https://user-images.githubusercontent.com/69050562/119224076-0fd45d00-bafd-11eb-808a-04cbecd1a0c4.PNG)
### Receiver MCU (on the Ronin M)
- I read here https://forum.dji.com/thread-167232-1-1.html that the power can come directly from the gimbal
- small MCU which can get powered by 5V
- protocol must haves:
  - TX -> Ronin
  - SPI -> NRF24
### Controller MCU (on the handle bar)
- Powered by a 18650 LiIon cell
  - needs a charging circuit board with USB + protection Circuit + LDO
- protocol must haves:
  - I²C -> MPU6050
  - SPI -> NRF24
  - multiple analog Pins -> Joystick

---
