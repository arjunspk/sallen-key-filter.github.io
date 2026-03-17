1. Project Goal
  * Primary Objective: Design and implement an active 4th-order Sallen-Key bandpass filter.
  * Target Frequency: Detect and isolate a 10 kHz signal.
  * Noise Rejection: Attenuate interference from unwanted frequencies at 17 kHz and 25 kHz.

2. Design Specs & Topology
  * Why Sallen-Key? Chosen for its simplicity, high input impedance, and stable gain, making it ideal for audio-frequency signal detection.
  * Why 4th-Order? A single 2nd-order stage did not provide a sharp enough "roll-off." By cascading two 2nd-order stages, I doubled the slope (reaching 80 dB per decade), which ensures much tighter filtering around the 10 kHz peak.
  * Gain and Q: The Quality Factor (Q) was tuned to provide a narrow bandwidth without causing instability or excessive ringing.

3. Components Used
   * Operational Amplifiers: TL081 (chosen for low noise and high-speed JFET inputs).
   * Passives
       * Resistors (R): Used precise values (calculated for 10 kHz center frequency).
       * Capacitors (C): Ceramic capacitors chosen for stability.
   * Testing Equipment: * LTspice for pre-build verification.
       * MATLAB for theoretical transfer function plotting.
       * Oscilloscope & Function Generator for physical frequency response analysis.

 4. The Engineering Process
    * Hand Calculations: Used the Sallen-Key transfer function formula to determine component values.
    * Simulation: Verified the design in LTspice to check the Bode plot and phase margin.
    * Physical Build: Assembled the circuit on a breadboard, paying close attention to ground loops and noise.
    * Verification: Used the Frequency Response Analyzer (FRA) feature on the oscilloscope to compare the physical hardware output against the SPICE model.

 5. Measured Results
    * Simulation Peak: Predicted 10 kHz.
    * Physical Peak: Measured 10.15kHz.
    * Attenuation Performance: Successfully dropped the 17 kHz signal by ~18dB and the 25kHz signal by ~36dB
    * Conclusion: The project successfully demonstrated how cascading filter stages increases selectivity and improves signal-to-noise ratio in signal detection systems.






   
     
     
        



