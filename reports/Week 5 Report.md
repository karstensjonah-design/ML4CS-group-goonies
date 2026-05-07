# Week 01 Report — Machine Learning for Smart and Connected Systems (ML4SCS)

## Weekly Goal
-Den Tobii EyeTracker 5 ausprobieren und mit Datenextrahierung auseinandersetzen
-Daten aus AIrpods extrahieren und überlegen wie wir diese einsetzen
-Texte und Fragen für Experiment ausarbeiten

## Work Done This Week

### 0. Project setup
Project Question: 
  -Inwiefern lassen sich Blickbewegungsdaten (Tobii ET5) und Kopf-Kinematik (AirPods Motion Data) kombinieren, um die kognitive Konzentration während einer Leseaufgabe vorherzusagen?
Test SetUp: 
  -Probant liest 5 Texte von jeweils 3-5 Minuten und muss zu jedem Text ca 10. fragen beantworten. Texte müsse bei hohre Konzentration gerade so in dem Zeitintervall lesbar sein.

### 1. Data Work
-Erste Bewegungsdaten wurden mit den Airpods gesammelt. Einmal wurde isch dabei kkaum bewegt, um Konzentration zu simulieren. Beim zweiten mal wurde sich mehr bewegt um ein unruhiges/unkonzentriertes VErhalten zu simulieren.

### 2. Analysis / Modeling Work
-Die Beiden Bewegungsdaten der AirPods wurden in Pythen ausgwertet und visualisiert:
============================================================
FEATURE-VERGLEICH
============================================================
label            T-1 (ruhig)  T-2 (unruhig)
lin_x_mean          0.391665       0.366826
lin_x_std           0.007314       0.100182
lin_x_max           0.406608       2.194857
lin_y_mean         -0.056081      -0.078607
lin_y_std           0.014745       0.145019
lin_y_max           0.211307       0.506687
lin_z_mean          0.915091       0.907165
lin_z_std           0.005032       0.048346
lin_z_max           1.004216       1.093162
magnitude_mean      0.997104       0.997956
magnitude_std       0.004074       0.034161
magnitude_max       1.070350       2.197377
movement_events   880.000000     881.000000
stillness_ratio     0.000000       0.000000
rot_x_mean          0.000945      -0.000770
rot_x_std           0.047478       0.306279
rot_x_max           0.629113       2.910680
rot_y_mean         -0.000879       0.000625
rot_y_std           0.029686       0.268412
rot_y_max           0.495701       3.068207
rot_z_mean          0.000673       0.002375
rot_z_std           0.068925       0.413729
rot_z_max           1.114646       4.043236
pitch_mean         -0.056015      -0.081074
pitch_std           0.013558       0.143388
pitch_range         0.128817       0.952362
roll_mean          -0.403830      -0.386318
roll_std            0.007291       0.102712
roll_range          0.116575       1.867424
yaw_mean            0.033825      -0.774879
yaw_std             0.018406       0.166281
yaw_range           0.250519       1.946795

============================================================
ZUSAMMENFASSUNG
============================================================
magnitude_mean-Durchschnittliche Bewegungsstärke                            ruhig=0.9971  unruhig=0.9980  Δ=+0.1%
magnitude_std-Schwankung der Bewegungsstärke                                ruhig=0.0041  unruhig=0.0342  Δ=+738.5%
stillness_ratio-Anteil echter Ruhe-Momente                                  ruhig=0.0000  unruhig=0.0000  Δ=+0.0%
pitch_range-pitch_range — Gesamtbereich der Vor-/Rückneigung                ruhig=0.1288  unruhig=0.9524  Δ=+639.3%
yaw_range-Gesamtbereich der Links-/Rechtsdrehung                            ruhig=0.2505  unruhig=1.9468  Δ=+677.1%

Es ist ein klarer Unterschied zwischen ruhigem und unruhigem Verhalten erkennbar. 

Taugt zur Unterscheidung?
magnitude_mean	Nein (0.1% Unterschied)
magnitude_std	Ja (738%)
stillness_ratio	Nein (Schwellenwert zu niedrig)
pitch_range	Ja (639%)
yaw_range	Ja (677%)

### 3. Repository / Documentation Work
- What was added to GitHub?
- Which files or folders were created?


## Challenges
- Eigeninitiative

## Key Insights
-Wie man AirPod daten bekommt/benutzt

## Plan for Next Week
-Tobi EyeTracker 5 SetUp
-Quellarbeit
-Test genauer definieren

## Contributions
- Member 1: AirPods Anlayse
