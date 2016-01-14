#fpsplib

Fuzzy extension to the Project Scheduling Library PSPLIB single mode problems.

Base files can be downloaded here:

http://www.om-db.wi.tum.de/psplib/getdata.cgi?mode=sm


The .fz files contain one line per activity. Each line consists of 3 values separated by spaces.
Each line defines a beta distribution for the delay of each acitivy. The source and sink acitivities always have three zeros as they always have zero duration.
Each line contains the following parameters:

maximumDelay Alpha Beta

The maximumDelay defines the range of the beta distribution. So each activity's duration is distributed between the original duration from PSPLIB + the beta distributed delay with parameters Alpha and Beta.

The duration of an activity can hence be sampled using:

sampledDuration = originalDuration + maximumDelay * BetaSample(Alpha, Beta)

Contact: 

Maximilian Bügler <max.buegler@tum.de>
