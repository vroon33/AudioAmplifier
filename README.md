# Audio Amplifier Circuit

![Full Circuit](Full%20Circuit.png)

This audio amplifier was designed as part of the H1 Project for S25 Spring Semester, Electronics-Workshop II Course, at IIIT Hyderabad. The project was designed by [Vedant Pahariya](https://github.com/VedantPahariya) and  [Varun Shastry](https://github.com/vroon33).

This repository holds the LTSpice schematics, reference books and manuals, the images of the final circuit, and the oscilloscope readings of the circuit. The circuit was designed to amplify audio signals of 5mV-10mV signals to 2V-4V signals so as to drive the speaker load of 10 ohms, with a power rating of 0.5W.

Givem such a small signal input, the circuit has 4 main stages, the `Preamp`, the `Gain stage`, the `Active Bandpass Filter`, and the `Power Amplifier`. Use of buffers were not allowed to isolate stages, so methods for impedance matching were utilised.

## Preamp

The preamp is a dual-input unbalanced output configuration, such that it has a high CMRR measure and eliminates common-mode noise. The preamp is designed to have a gain of about 20. Bias points were chosen based on a current value through the transistors, and then calculating the other parameters through theory. Power supply constraints were limited to +/- 5V.

## Gain Stage

The gain stage is a common-emitter amplifier with a gain such that the output is a 8.2Vpp for the 20mVpp input. The biasing was done to ensure that the transistor operates in the active region. The gain stage was designed with the impedance matching factor in mind. Power supply was limited to +/- 5V.

## Active Bandpass Filter

The active bandpass filter was designed to filter out the noise and the DC offset from the signal. The filter was designed to have a gain of 1, and a bandwidth of 20Hz-20kHz, to retain the audio signals. The filter roll-off was chosen to be -40dB/decade, using a cascaded second order filter. For the proper operation of the op-amp, a power supply of +/- 12V was used.

## Power Amplifier

The power amplifier was designed to drive the speaker load of 10 ohms, with a power rating of 0.5W. The power amplifier was designed to have no gain! The Class AB  with current-source diode biasing topology was utilised because of the voltage supply of +/- 5V being very close to the input voltage of 4.1V. The power amplifier was designed to have a high current gain to drive the speaker load.

## Final Circuit

The final circuit was designed to have a gain of 400-430, and the best power output of 0.7W. The circuit was designed to have a **THD of just 3%**, with the hardware having a **THD of about 10%**. The circuit was designed to have a bandwidth of 20Hz-20kHz, and the output was tested with a 10 ohm speaker load.

We have also provided a detailed report of the project, which includes the theory, the design, the simulation, and the testing of the circuit. The report also includes the references used for the project.
