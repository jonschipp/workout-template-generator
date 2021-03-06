# Time to Train

A generator for customizable workout templates using spreadsheets. The spreadsheets are compatible with Google Sheets.

This is a new project which will make it incredibly easy to create exercise programs. Import them in Google Sheets and share with your clients and friends.

```
$ ./timetotrain.py --weeks 8 --frequency 3 --slots 3 --sets 10 --filename train.xlsx
Writing sheet Week 1
Writing sheet Week 2
Writing sheet Week 3
Writing sheet Week 4
Writing sheet Week 5
Writing sheet Week 6
Writing sheet Week 7
Writing sheet Week 8
Writing program to train.xlsx
```

![Sheet Example](imgs/sheet.png)

## Install

```
pip3 install openpyxl
git clone https://github.com/jonschipp/timetotrain
```

## Metrics

The generated template includes the following metrics.

* Sums for Load, Reps, RIR, RPE, Avg Velocity, and Int % - calculated per exercise slot
* Averages for Load, Reps, RIR, RPE, Avg Velocity, and Int % - calculated per exercise slot
* Volume (Sets x Reps) - calculated per exercise slot
* Tonnage (Sets x Reps x Load) - calculated per exercise slot
* E1RM - [Epley equation](https://www.vcalc.com/wiki/vCalc/Epley+Formula+%281+rep+max%29)
* Intensity Percentage per set (Int % of E1RM) - Requires manual E1RM input
* Average RPE - Average RPE of all exercise slots in a day
* Session RPE - manual input
* Internal Load (Sets * Session RPE) - Used to track training adjustments. Keep below a ~10% load increase on average week to week. See "Nutritional and Logistical Strategies for Reducing Illness", Eric Helms, MASS Research Review Vol. 3, Issue 2, February 2019

More to come!
