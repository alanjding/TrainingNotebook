# TrainingNotebook
A Jupyter Notebook for myself to use to track components of my training. Using it is, admittedly, not the most straightforward task: you will need to set up your own Strava app and configure all the code-stringy-things yourself in one of the first few cells

A Jupyter Notebook that allows me to fetch and extensively analyze my running data from Strava. It can estimate acute and chronic training load as well as provide plots showing different performance metrics. The data fed into these plots can be filtered by traits such as sleep quality and motivation to run which the user provides daily to a questionnaire.

In particular, various streams from my Strava data (time-indexed lists of instantaneous statistics such as heart rate, distance covered, cadence) are pulled. The heart rate stream is ultimately used to arrive at a metric called “Form”, measuring training stress with respect to fitness. This is functionality available in existing training analytics software (such as TrainingPeaks); however, I had to recalculate it in this application to do further correlative analyses.

The above objective, formulaic approach to my training data is then combined with user inputted data on sleep quality, sleep time, soreness, and motivation, as well as temperature and dew point data. The application can generate histograms and run Gaussian mixture models on aggregated pace and heart rate stream data. On the other hand, the user inputted data is correlative analyses between any two of these variables, in addition to the run’s date, distance, time of day, form, or deviation from expected heart rate. Expected heart rate for a run, knowing its pace, is obtained by converting the pace to a percentile, and getting the heart rate corresponding to that percentile.

The point of the application is to quantify the effectiveness of any training that I do and catch signs of overtraining/burnout earlier (form, drops in performance unrelated to external factors, consistently positive deviation from expected heart rate, etc.)

I've intended for a while to add a feature that constrains the data being passed into the graph but found relatively little utility in doing that in the scope of my own needs. You will hence find an extended commented out section of some range slider widgets that would otherwise do nothing other than enable you to fidget with them.
