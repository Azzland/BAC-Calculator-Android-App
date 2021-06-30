# BAC-Calculator-Android-App

Inspired by online BAC calculators I have used my Python programming skills to create my own Android application which calculates the blood alcohol concentration (BAC) based on personal characteristics (height, weight, age, gender, full or empty stomach), the time the drinking started, the current time and details of all drink types including volume and alcohol content as a percentage.

The app was constructed using the Python Kivy library. It was constructed using button, text input and label widgets and the box layout method was used. Google Colab coding was used to deploy the app.

The Widmark formula modified by the research of Posey and Mozayani in 2007 was used to estimate the BAC.

The Widmark formula is the most common method to estimate the BAC and was developed by Swedish scientist Erik Widmark in 1932 (Brouwer 2004). Most BAC calculators online use this formula or their own variations of it.

C = A/rW – Bt         (Posey and Mozayani 2007)

Where C is the blood alcohol concentration, A is the mass of alcohol consumed (g), r is the Widmark factor, W is the body weight (g), t is the time elapsed since drinking (hours) and B is the alcohol elimination rate (typically 0.015).

The Widmark factor is typically 0.68 for males and 0.55 for females, both varying by plus or minus 0.11 (Posey and Mozayani 2007). The Widmark factor is dependent on weight, gender, body fat and age. This can be accurately determined by calculating the total body water (TBW) of the individual using a formula developed by Watson in 1980. The formulae are as follows.

TBW(male) = 2.447 – 0.09156*age + 0.1074*height + 0.3362*weight.

TBW(female) = -2.097 + 0.1069*height + 0.2466*weight

Where age is in years, height is in cm and weight is in kg (Koperska 2020). The TBW is divided by the average weight to volume ratio of water in blood to give the Widmark constant r (Posey and Mozayani 2007).

Posey and Mozayani in 2007 found that the presence of food in the stomach after eating can influence the rate of alcohol adsorped and the BAC. They modified the Widmark formula by including a rate constant, k, which is 6.5/hour for an empty stomach and 2.3/hour for a full stomach. The formula becomes.

C = A(1 – exp(-kt))/rW – Bt


# References
Posey, D., & Mozayani, A. (2007). The estimation of blood alcohol concentration : Widmark revisited. Forensic science, medicine, and pathology, 3(1), 33–39.

Brouwer I. G. (2004). The Widmark formula for alcohol quantification. SADJ : journal of the South African Dental Association = tydskrif van die Suid-Afrikaanse Tandheelkundige Vereniging, 59(10), 427–428.

Koperska M. (2020). Total Body Water Calculation https://www.omnicalculator.com/health/body-water Omni.
