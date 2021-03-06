# cr-analysis, python package for circadian analysis!
**01/07/2020 cr-analysis 3.0.0 is available now!**

```py
pip install cr-analysis
from cr_analysis.main import visualizer

# Prepare the csv file. E.g. sample1.csv
# E.g. 
visualizer('sample1.csv', file_path = '/content/drive/My Drive/')
```


## Description
This is the tool to make a graph.
Peak detection and period determination will be available
Detect the peaks, and detemine the periods.

### P.S.
ver3 only has graphing function.

Other functions will come soon.

## Settings

```py
# graph_settings
settings = {
    "x_axis_title" : "Time [h]",
    "y_axis_title" : "Bioluminescence",
    "column_number" : 5,
    "overwrite_column_number" : 4,
    "y_axis_share_switch" : 1,
    "yaxis_percentage_switch" : 1,
    "over_view_image_length" : 4.5,
    "over_view_image_width" : 5.0,
    "all_plot_column_number" : 12,
    "all_plot_image_length" : 2.5,
    "all_plot_image_width" : 2.5
}


settings_2 = {
    0 : ["black", "Group0"],
    1 : ["red", "Group1"],
    2 : ["orange", "Group2"],
    3 : ["green", "Group3"],
    4 : ["lightgreen", "Group4"],
    5 : ["blue", "Group5"],
    6 : ["lightblue", "Group6"],
    7 : ["orangered", "Group7"],
    8 : ["salmon", "PGroup8"],
    9 : ["forestgreen", "Group9"],
    10 : ["limegreen", "Group10"],
}


setting_3 = {}



visualizer(file_name, # include .csv -> sample.csv
               file_path = "", # /content/sample.csv -> /content/
               graph_settings = settings,
               subtitle_and_color = settings_2,
               overlap_dict = setting_3,
               file_from = 1, #If the data comes from Lumicec, set 0. Default is 1.
               sampling_period = 60,
               estimated_period = 24,
               over_view_plot_switch = 1,
                all_plot_switch = 1
    )
```

## Demo
Overview plot:
![overview](https://user-images.githubusercontent.com/45617592/72204708-49836580-34be-11ea-8505-9f72830e9326.png)

All plot:
![allplot](https://user-images.githubusercontent.com/45617592/72204687-fb6e6200-34bd-11ea-8c45-f70e922c9b90.png)
