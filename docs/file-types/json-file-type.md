# VOSviewer JSON files

VOSviewer JSON files are JSON files for storing a network. These files can also store a configuration of VOSviewer Online to be used for visualizing the network.

## JSON format

### Top level

Attribute | Type | Description
--------- | ---- | -----------
network | Object | [Network](#network-object) object representing a network.
config | Object | [Config](#config-object) object specifying a configuration of VOSviewer Online to be used for visualizing the network.
info | Object | [Info](#info-object) object providing information about the visualization of the network.

### Network object

Attribute | Type | Description
--------- | ---- | -----------
items | Array | Array of [Item](#item-object) objects, each representing an item in a network.
links | Array | Array of [Link](#link-object) objects, each representing a link in a network.
clusters | Array | Array of [Cluster](#cluster-object) objects, each representing a cluster of items in a network.

### Item object

Attribute | Type | Description
--------- | ---- | -----------
id | String or integer | ID of an item.
label | String | Label of an item.
description | String | Description of an item. A description may include HTML formatting.
url | String | URL of an item.
x | Float | Horizontal coordinate of an item.
y | Float | Vertical coordinate of an item.
cluster | Integer | Cluster to which an item belongs. A cluster is represented by an integer between 1 and 1000.
weights | Object map of key-value pairs | Weights of an item. Each weight is represented by a key and a value. The key is a string. The value is a non-negative number. For example: `"weights": { "Publications": 190, "Citations": 4213, "Norm. citations": 314.2 }`.
scores | Object map of key-value pairs | Scores of an item. Each score is represented by a key and a value. The key is a string. The value is a number.

### Link object

Attribute | Type | Description
--------- | ---- | -----------
source_id | String or integer | ID of a source item.
target_id | String or integer | ID of a target item.
strength | Float | Strength of the link between a source item and a target item. The strength is a non-negative number.

### Cluster object

Attribute | Type | Description
--------- | ---- | -----------
cluster | Integer | Cluster. A cluster is represented by an integer between 1 and 1000.
label | String | Label of a cluster.

### Config object

Attribute | Type | Description
--------- | ---- | -----------
color_schemes | Object | [Color_schemes](#color_schemes-object) object specifying custom color schemes used by VOSviewer Online.
parameters | Object | [Parameters](#parameters-object) object specifying parameters used by VOSviewer Online.
terminology | Object | [Terminology](#terminology-object) object specifying terminology used by VOSviewer Online.
templates | Object | [Templates](#templates-object) object specifying templates used by VOSviewer Online.
styles | Object | [Styles](#styles-object) object specifying styles used by VOSviewer Online.

### Color_schemes object

Attribute | Type | Description
--------- | ---- | -----------
cluster_colors | Array | Array of [Cluster_color](#cluster_color-object) objects, each representing a cluster and the corresponding color.
score_colors | Array | Array of [Score_colors](#score_colors-object) objects, each representing a rescaled score and the corresponding color.

### Cluster_color object

Attribute | Type | Description
--------- | ---- | -----------
cluster | Integer | Cluster. A cluster is represented by an integer between 1 and 1000.
color | String | Color of a cluster. A color is represented by a hexadecimal code (e.g., `#ee3e80`).

### Score_color object

Attribute | Type | Description
--------- | ---- | -----------
rescaled_score | Float | Rescaled score. A rescaled score is a number between 0 and 1.
color | String | Color of a rescaled score. A color is represented by a hexadecimal code (e.g., `#ee3e80`).

### Parameters object

Attribute | Type | Description
--------- | ---- | -----------
attraction | Integer | Value of the [**Attraction**](/docs/user-interface/control-panel/#attraction-and-repulsion) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
repulsion | Integer | Value of the [**Repulsion**](/docs/user-interface/control-panel/#attraction-and-repulsion) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
largest_component | Boolean | A network may consist of multiple components. When the layout of a network is created or updated, the network can be reduced to its largest component or the full network can be kept.
resolution | Float | Value of the [**Resolution**](/docs/user-interface/control-panel/#resolution) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
min_cluster_size | Integer | Value of the [**Minimum cluster size**](/docs/user-interface/control-panel/#minimum-cluster-size) parameter on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
merge_small_clusters | Boolean | Value of the [**Merge small clusters**](/docs/#merge-small-clusters) switch on the [**Update**](/docs/user-interface/control-panel/#update) tab in the [control panel](/docs/user-interface/control-panel/).
scale | Float | Value of the [**Scale**](/docs/user-interface/control-panel/#scale) slider on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
item_size | Integer | Value of the [**Size**](/docs/user-interface/control-panel/#size) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) (1 for the first option, 2 for the second option, etc.).
item_color | Integer | Value of the [**Color**](/docs/user-interface/control-panel/#color) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) (1 for the first option, 2 for the second option, etc.).
item_size_variation | Float | Value of the [**Size variation**](/docs/user-interface/control-panel/#size-variation) slider for items on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
max_label_length | Integer | Value of the [**Maximum label length**](/docs/user-interface/control-panel/#maximum-label-length) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
link_size_variation | Float | Value of the [**Size variation**](/docs/user-interface/control-panel/#size-variation_1) slider for links on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
min_link_strength | Float | Value of the [**Minimum strength**](/docs/user-interface/control-panel/#minimum-strength-and-maximum-links) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
max_n_links | Integer | Value of the [**Maximum links**](/docs/user-interface/control-panel/#minimum-strength-and-maximum-links) parameter on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
curved_links | Boolean | Value of the [**Curved links**](/docs/user-interface/control-panel/#curved-links) switch on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/).
score_colors | String | Value of the [**Score colors**](/docs/user-interface/control-panel/#score-colors) drop down list on the [**View**](/docs/user-interface/control-panel/#view) tab in the [control panel](/docs/user-interface/control-panel/) ('Viridis', 'Plasma', 'Rainbow', 'White-blue-purple', 'White-yellow-green-blue', 'White-yellow-orange-red', 'Coolwarm', or 'Spectral').
min_score | Float | Value of the **Min. score** parameter in the legend.
max_score | Float | Value of the **Max. score** parameter in the legend.
zoom_level | Float | Initial zoom level of the visualization in the [main panel](/docs/user-interface/main-panel/). The zoom level has a value of at least 1.
show_info | Boolean | When opening a network, show or do not show information about the visualization of the network.
show_item | String | Item on which the visualization in the [main panel](/docs/user-interface/main-panel/) will be zoomed in. The item is designated by its label.
simple_ui | Boolean | Simple or normal user interface. The use of the simple user interface is recommended when [embedding a visualization in a webpage](/docs/sharing/embedding/).
dark_ui | Boolean | Dark or light user interface.

### Terminology object

Attribute | Type | Description
--------- | ---- | -----------
item | String | Term used to refer to an item (singular).
items | String | Term used to refer to an item (plural).
link | String | Term used to refer to a link (singular).
links | String | Term used to refer to a link (plural).
cluster | String | Term used to refer to a cluster (singular).
clusters | String | Term used to refer to a cluster (plural).
link_strength | String | Term used to refer to the strength of a link.
total_link_strength | String | Term used to refer to the total link strength of an item.

### Templates object

Attribute | Type | Description
--------- | ---- | -----------
item_description | String | Template for the description of an item.
link_description | String | Template for the description of a link.

### Styles object

Attribute | Type | Description
--------- | ---- | -----------
description_heading | String | CSS style for headings in the description of an item or a link.
description_label | String | CSS style for labels in the description of an item or a link.
description_text | String | CSS style for text in the description of an item or a link.
description_url | String | CSS style for URLs in the description of an item or a link.

### Info object

Attribute | Type | Description
--------- | ---- | -----------
title | String | Title of the visualization of a network.
description | String | Description of the visualization of a network. A description may include HTML formatting.

## Example

This is an example of a VOSviewer JSON file:

```
--8<-- "docs/assets/data/example.json"
```

The above JSON file can be downloaded [here](/docs/assets/data/example.json).

Providing the JSON file as input to VOSviewer Online yields the following visualization:

<iframe allowfullscreen="true" src="https://app.vosviewer.com/?json=https://app.vosviewer.com/docs/assets/data/example.json&simple_ui=true" width="100%" height="75%" style="border: 1px solid #ddd; max-width: 1200px; min-height: 500px"></iframe>
