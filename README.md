# ITESO-phd-IDI10
Neural Network  to predict Temperatures in Kelvin scale using Radiometric Images 
  * 150 K Radiometric Files Used 
  * 15 M Of Records generated
  * 26 K Unique records found
  
  Install **exiftools** to extract Radiometric Tags fom JPEG file
  
Featues used to train the NN:
   * Raw = if Endian is LITTLE-ENDIAN then (RAW_VAL >> 8) + ((RAW_VAL & 0x00ff) << 8 else RAW_VAL
   * Distance
   * Emissivity
   * ReflectedApparentTemperature
   * AtmosphericTemperature
   * IRWindowTemperature
   * IRWindowTransmission
   * RelativeHumidity
   * PlanckB
   * PlanckF
   * PlanckO
   * PlanckR1
   * PlanckR2
   * AtmosphericTransAlpha1
   * AtmosphericTransAlpha2
   * AtmosphericTransBeta1
   * AtmosphericTransBeta2
   * AtmosphericTransX
  
  Models in H5 generated in  Tensor Flow 2.5
   * 16x16x16x1-F18.h5    trained with all 18  features
   * 16x16x16x1-F10.h5    trained with features with multiple values.
    
  Tested on Radiometric Images using FLIR(c) Pro Gen 3, A310 series, AX8.
  
  FLIR(c) Is a trademark of Teledyne FLIR
  

