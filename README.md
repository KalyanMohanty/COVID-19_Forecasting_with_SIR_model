# Forecasting_with_SIR_mode
Kaggle Competition Link:
https://www.kaggle.com/kalyanmohanty/forecasting-with-sir-model

# Introduction:

Coronavirus disease 2019 (COVID-19) is an infectious disease caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). The disease was first identified in December 2019 in Wuhan, the capital of China's Hubei province, and has since spread globally, resulting in the ongoing 2019–20 coronavirus pandemic. Common symptoms include fever, cough, and shortness of breath. Other symptoms may include fatigue, muscle pain, diarrhea, sore throat, loss of smell, and abdominal pain. While the majority of cases result in mild symptoms, some progress to viral pneumonia and multi-organ failure. As of 25 April 2020, more than 2.7 million cases have been reported in more than 200 countries and territories, resulting in more than 1,95,920 deaths. More than 781382 people have recovered.
<p align="center">
  <img width="460" height="300" src=Images/corona_virus_color.jpg>
</p>

# Transmission:
Some details about how the disease is spread are still being determined. The WHO and CDC say it is primarily spread during close contact and by small droplets produced when people cough, sneeze or talk; with close contact being within 1–3 m (3 ft. 3 in–9 ft. 10 in). A study in Singapore found that uncovered coughing can lead to droplets traveling up to 4.5 meters (15 feet). A second study, produced during the 2020 pandemic, found that advice on the distance droplets could travel might be based on old 1930s research which ignored the protective effect and speed of the warm moist outbreath surrounding the droplets; it advised that droplets can travel around 7–8 meters. 

# Objective:

The objective of this work is to analyze susceptible, Infectious, and recovered using the SIR model.

# Total Population

The highly populated country has more chances to get infected quickly. The following are top populated countries across the globe.
 <p align="center">
  <img width="460" height="300" src=Images/popu.JPG>
</p>

# The number of the day goes out

There are different age groups people who go outside on different days. So here we have analyzed which age group has most days outside the home. The more they go outside can have more chances to infected by the COVID-19 virus. 
<p align="center">
  <img width="460" height="300" src=Images/age_perce.JPG>
</p>
 
The people of age group 26 – 65 go outside approximately 5 or 6 days a week. So they can get in contact with other infected people as compared to another age group. 

# Grouping by growth factor
The number of confirmed cases is increasing in many countries, but there are two countries. In a first-type country, the growth factor is larger than 1 and the number of cases is rapidly increasing. In a second-type country, the growth factor is less than 1.
Calculate the growth factor

                                       Growth Factor =  (ΔC_n )/(ΔC_(n-1) )
Where C is the number of confirmed cases
	Out breaking: growth factor >> 1 for the last 7 days
	Stopping: growth factor << 1 for the last 7 days
	At a crossroad: the others
# Group 1: Out breaking, growth factor >> 1 for the last 7 days
<p align="center">
  <img width="460" height="300" src=Images/gp1_outbreaking.JPG>
</p>
 
# Group 2: Stopping, growth factor << 1 for the last 7 days
 
 <p align="center">
  <img width="460" height="300" src=Images/gp2_stopping.JPG>
</p>

# Group 3: The others

 <p align="center">
  <img width="460" height="300" src=Images/gp3_crossend.JPG>
</p>

# SIR Model
A SIR model is an epidemiological model that computes the theoretical number of people infected with a contagious illness in a closed population over time. The name of this class of models derives from the fact that they involve coupled equations relating the number of susceptible people S (t), number of people infected I (t), and number of people who have recovered R (t). One of the simplest SIR models is the Kermack - McKendrick model
<p align="center">
  <img width="460" height="300" src=Images/5cacd542832adc4f625fae17_SIR-Analysis-illustration.png>
</p>

# Non-dimensional SIR model

To simplify the model, we will remove the units of the variables from ODE (Ordinary Differential Equation).

                                       Set (S, I, R) = N × (x, y, z) and (T, β, γ) = (τt, τ -1ρ, τ −1σ)
                                       dx/dt = -ρxy                                                  (1)
                                       dy/dt = -ρxy- σy                                              (2)
                                       dz/dt = σy                                                    (3)
				       
Where N is the total population and τ is a coefficient ([min], is an integer to simplify).
The range of variables and parameters:

                                        0 ≤ (x, y, z, ρ, σ ) ≤ 1
                                        1 ≤ τ ≤ 1440
Basic reproduction number, Non-dimensional parameter, is defined as

                                        R0 = ρσ−1 = βγ−1
					
Estimated Mean Values of R0:
R0 means "the average number of secondary infections caused by an infected host" When 

X=1/R_0 =dy/dt =0                                                                                              (4)
<p align="center">
  <img width="460" height="300" src=Images/sir.JPG>
</p>

(Global prediction using the SIR model.  X: Susceptible, Y: Infected, Z: Recovered)

# India
India seems to get its peak around the first week of May after that the number of cases will slow down.

<p align="center">
  <img width="460" height="300" src=Images/india_active.JPG>
</p>
 
# China
China got its peak after 39 days of the first case then after around 30 days the curve flattened. 
 
 <p align="center">
  <img width="460" height="300" src=Images/china_active.JPG>
</p>

# Remark:
China got its peak after 30 days. Compared to china India will get its peak after 50 days of its first case which shows a better result
