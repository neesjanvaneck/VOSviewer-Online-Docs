# Linking to a visualization

A visualization of a network in VOSviewer Online can be shared by linking to the visualization.

## Creating a link

Consider the network stored in the following [VOSviewer JSON file](/docs/file-types/json-file-type/):

```
https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.json
```

This is a link to a visualization of this network in VOSviewer Online:

```
https://app.vosviewer.com/?json=https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.json&scale=1.5&curved_links=false
```

Using this link, VOSviewer Online is launched, the above network is opened, and a visualization of the network is presented. In addition, the [**Scale**](/docs/user-interface/control-panel/#scale) slider on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) is set to `1.5`. The [**Curved links**](/docs/user-interface/control-panel/#curved-links) switch is set to `false`.

Instead of a [VOSviewer JSON file](/docs/file-types/json-file-type/), it is also possible to use a [VOSviewer map and network file](/docs/file-types/map-and-network-file-type/). Consider the network stored in the following map and network file:

```
https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_map.txt
https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.txt
```

The following link can be used to launch VOSviewer Online and to open and visualize this network:

```
https://app.vosviewer.com/?map=https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_map.txt&network=https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.txt&scale=1.5&curved_links=false
```

Using this link, the [**Scale**](/docs/user-interface/control-panel/#scale) slider is again set to `1.5` and the [**Curved links**](/docs/user-interface/control-panel/#curved-links) switch is again set to `false`.

The above links include the parameters `json`, `map`, `network`, `scale`, and `curved_links`. The full list of parameters supported by VOSviewer Online can be found below.

To simplify a link, you may consider the use of a URL shortening service, such as [Bitly](https://bitly.com/){target="_blank"} or [TinyURL](https://tinyurl.com/){target="_blank"}.

## Using Google Drive

It is often convenient to use a cloud storage service to link to a visualization. We consider the use of Google Drive, although alternatives such as Microsoft OneDrive and Dropbox can be used as well. The use of Google Drive requires a Google account.

The first step is to upload a [VOSviewer JSON file](/docs/file-types/json-file-type/) to Google Drive and to get a link for sharing the file. To obtain a suitable link, select the **Anyone with the link** option, not the **Restricted** option. Also, select the **Viewer** option, not the **Commenter** or **Editor** option. The following link may for instance be obtained:

```
https://drive.google.com/file/d/16rdPZ3Md3b3mbsIftRZRjEUM6kkFX2zy/view?usp=sharing
```

This is a link for viewing the JSON file in a web browser.

The second step is to convert this into a link for downloading the JSON file. In the case of the above link, the corresponding link for downloading the JSON file is:

```
https://drive.google.com/uc?id=16rdPZ3Md3b3mbsIftRZRjEUM6kkFX2zy
```

Hence, the link `https://drive.google.com/file/d/XXX/view?usp=sharing` is converted into the link `https://drive.google.com/uc?id=XXX`, where `XXX` denotes the identifier of a JSON file on Google Drive.

The final step is to create a link for launching VOSviewer Online and for opening and visualizing the network stored in the JSON file:

```
https://app.vosviewer.com/?json=https://drive.google.com/uc?id=16rdPZ3Md3b3mbsIftRZRjEUM6kkFX2zy
```

The above link includes only the parameter `json`. Additional parameters may be added. The full list of parameters supported by VOSviewer Online is presented below.

Instead of taking the above steps, it is also possible to use the share feature in the stand-alone version of VOSviewer. In addition to Google Drive, this feature also supports Microsoft OneDrive and Dropbox.

## Parameters for opening a network

Parameter | Description
--------- | -----------
json | [VOSviewer JSON file](/docs/file-types/json-file-type/) that is provided as input to VOSviewer Online.
map | [VOSviewer map file](/docs/file-types/map-and-network-file-type/#vosviewer-map-files) that is provided as input to VOSviewer Online.
network | [VOSviewer network file](/docs/file-types/map-and-network-file-type/#vosviewer-network-files) that is provided as input to VOSviewer Online.

## Parameters for creating or updating the layout and clustering of a network

Parameter | Description
--------- | -----------
attraction | Value of the [**Attraction**](/docs/user-interface/control-panel/#attraction-and-repulsion) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
repulsion | Value of the [**Repulsion**](/docs/user-interface/control-panel/#attraction-and-repulsion) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
largest_component | A network may consist of multiple components. When the layout of a network is created or updated, the network can be reduced to its largest component ('true') or the full network can be kept ('false').
resolution | Value of the [**Resolution**](/docs/user-interface/control-panel/#resolution) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
min_cluster_size | Value of the [**Minimum cluster size**](/docs/user-interface/control-panel/#minimum-cluster-size) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
merge_small_clusters | Value of the [**Merge small clusters**](/docs/#merge-small-clusters) switch on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/) ('true' or 'false').

## Parameters for adjusting the visualization of a network

Parameter | Description
--------- | -----------
scale | Value of the [**Scale**](/docs/user-interface/control-panel/#scale) slider on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
item_size | Value of the [**Size**](/docs/user-interface/control-panel/#size) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) (1 for the first option, 2 for the second option, etc.).
item_color | Value of the [**Color**](/docs/user-interface/control-panel/#color) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) (1 for the first option, 2 for the second option, etc.).
item_size_variation | Value of the [**Size variation**](/docs/user-interface/control-panel/#size-variation) slider for items on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
max_label_length | Value of the [**Maximum label length**](/docs/user-interface/control-panel/#maximum-label-length) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
link_size_variation | Value of the [**Size variation**](/docs/user-interface/control-panel/#size-variation_1) slider for links on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
min_link_strength | Value of the [**Minimum strength**](/docs/user-interface/control-panel/#minimum-strength-and-maximum-links) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
max_n_links | Value of the [**Maximum links**](/docs/user-interface/control-panel/#minimum-strength-and-maximum-links) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
curved_links | Value of the [**Curved links**](/docs/user-interface/control-panel/#curved-links) switch on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) ('true' or 'false').
score_colors | Value of the [**Score colors**](/docs/user-interface/control-panel/#score-colors) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) ('Viridis', 'Plasma', 'Rainbow', 'White-blue-purple', 'White-yellow-green-blue', 'White-yellow-orange-red', 'Coolwarm', or 'Spectral').
min_score | Value of the **Min. score** parameter in the legend.
max_score | Value of the **Max. score** parameter in the legend.
zoom_level | Initial zoom level of the visualization in the [main panel](/docs/user-interface/main_panel/). The zoom level has a value of at least 1.
show_item | Item on which the visualization in the [main panel](/docs/user-interface/main_panel/) will be zoomed in. The item is designated by its label.

## Parameters for adjusting the user interface of VOSviewer Online

Parameter | Description
--------- | -----------
simple_ui | Simple or normal user interface ('true' or 'false'). The use of the simple user interface is recommended when [embedding a visualization in a webpage](/docs/sharing/embedding/).
dark_ui | Dark or light user interface ('true' or 'false').
