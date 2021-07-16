# Control panel

The control panel consists of the following tabs:

- [**View**](#view). Use this tab to make adjustments to the visualization of a network in the [main panel](/docs/user-interface/main-panel/).

- [**Find**](#find). Use this tab to find an item in the visualization of a network in the [main panel](/docs/user-interface/main-panel/).

- [**Update**](#update). Use this tab to update the layout and clustering of the network visualized in the [main panel](/docs/user-interface/main-panel/).

## View

The **View** tab can be used to make adjustments to the visualization of a network in the [main panel](/docs/user-interface/main-panel/).

### Visualization

#### Scale

![Scale slider](/docs/assets/images/scale.png)

The **Scale** slider determines the scale of the visualization of a network. The higher the value of the slider, the larger the size of the items in the visualization and the thicker the links between the items.

### Items

#### Size

![Size drop down list](/docs/assets/images/size.png)

Use the **Size** drop down list to select the attribute that determines the size of items in the visualization of a network.

#### Color

![Color drop down list](/docs/assets/images/color.png)

Use the **Color** drop down list to select the attribute that determines the color of items in the visualization of a network.

#### Size variation

![Size variation slider](/docs/assets/images/size_variation.png)

The higher the value of the attribute selected in the **Size** drop down list, the larger the size of an item in the visualization of a network. The **Size variation** slider determines the strength of this effect.

#### Maximum label length

![Maximum label length parameter](/docs/assets/images/maximum_label_length.png)

The **Maximum label length** parameter determines the maximum length of a label displayed in the visualization of a network. If the length of the label of an item exceeds the maximum length, only the first part of the label is displayed.

### Links

#### Size variation

![Size variation slider](/docs/assets/images/size_variation.png)

The stronger the link between two items, the thicker the link in the visualization of a network. The **Size variation** slider determines the strength of this effect.

#### Minimum strength and Maximum links

![Minimum strength and Maximum links parameters](/docs/assets/images/minimum_strength_maximum_links.png)

The **Minimum strength** and **Maximum links** parameters determine, respectively, the minimum strength of the links displayed in the visualization of a network and the maximum number of links displayed in the visualization of a network. If the number of links that have the minimum strength exceeds the maximum number of links to be displayed, only the strongest links are displayed.

#### Curved links

![Curved links switch](/docs/assets/images/curved_links.png)

The **Curved links** switch determines whether links have a straight or a curved shape in the visualization of a network.

### Color schemes

#### Cluster colors

![Cluster colors](/docs/assets/images/cluster_colors.png)

When an attribute with categorical values (i.e., clusters) is selected in the **Color** drop down list, the **Cluster colors** options can be used to adjust the color scheme for coloring the items in the visualization of a network.

#### Score colors

![Score colors drop down list](/docs/assets/images/score_colors.png)

When an attribute with continuous values (i.e., scores) is selected in the **Color** drop down list, the **Score colors** drop down list can be used to select a color scheme for coloring the items in the visualization of a network. Eight color schemes are available.[^1] The default color scheme is **Viridis**.

[^1]: The color schemes available in VOSviewer Online have been obtained from Matplotlib, a plotting library for Python. Some color schemes have been slightly adjusted. For more information, see the [Matplotlib website](https://matplotlib.org/stable/tutorials/colors/colormaps.html){target="_blank"} and [this blog post](https://www.cwts.nl/blog?article=n-r2s274){target="_blank"}.

## Find

The **Find** tab can be used to find an item in the visualization of a network in the [main panel](/docs/user-interface/main-panel/).

Use the **Find item** text field to find an item in the network visualized in the [main panel](/docs/user-interface/main-panel/). Click on the item to zoom in on the item in the visualization of the network.

## Update

The **Update** tab can be used to update the layout and clustering of the network visualized in the [main panel](/docs/user-interface/main-panel/).[^2]

[^2]: For more information about the layout and clustering techniques used by VOSviewer Online, see [Van Eck et al. (2010)](https://doi.org/10.1002/asi.21421){target="_blank"}, [Waltman et al. (2010)](https://doi.org/10.1016/j.joi.2010.07.002){target="_blank"}, [Van Eck and Waltman (2014)](https://doi.org/10.1007/978-3-319-10377-8_13){target="_blank"}, and [Traag et al. (2019)](https://doi.org/10.1038/s41598-019-41695-z){target="_blank"}.

### Rotate / flip

#### Rotate

![Rotate button and Degrees to rotate text field](/docs/assets/images/rotate.png)

Use the **Rotate** button to rotate the layout of a network. The **Degrees to rotate** parameter determines the number of degrees by which the layout is rotated.

#### Flip horizontally

![Flip horizontally button](/docs/assets/images/flip_horizontally.png)

Use the **Flip horizontally** button to flip the layout of a network in horizontal direction.

#### Flip vertically

![Flip vertically button](/docs/assets/images/flip_vertically.png)

Use the **Flip vertically** button to flip the layout of a network in vertical direction.

### Normalization

#### Normalization method

![Normalization method drop down list](/docs/assets/images/normalization_method.png)

Use the **Normalization method** drop down list to determine how the strength of the links between the items in a network is normalized in the layout and clustering techniques used by VOSviewer Online:

- **No normalization**. Do not perform a normalization. In general, this is not recommended.

- **Association strength**. Use the association strength normalization method. Apart from a multiplicative constant, this method is identical to Eq. (6) in [Van Eck and Waltman (2009)](https://doi.org/10.1002/asi.21075){target="_blank"}. This option is selected by default.

- **Fractionalization**. Use the fractionalization normalization method. Apart from a multiplicative constant, this method is identical to Eq. (13) in [Van Eck and Waltman (2009)](https://doi.org/10.1002/asi.21075){target="_blank"}.

- **LinLog/modularity**. Use the same normalization as in the LinLog layout technique and the modularity clustering technique. For more information about these techniques, see [Newman (2004)](https://doi.org/10.1103/PhysRevE.69.066133){target="_blank"}, [Noack (2007)](https://doi.org/10.7155/jgaa.00154){target="_blank"}, and [Noack (2009)](https://doi.org/10.1103/PhysRevE.79.026102){target="_blank"}.

### Layout

#### Attraction and Repulsion

![Attraction and Repulsion text fields](/docs/assets/images/attraction_repulsion.png)

Use the **Attraction** and **Repulsion** parameters to adjust the layout of a network. The parameters must have a positive or negative integer value, typically between -2 and 2. The **Attraction** parameter must have a higher value than the **Repulsion** parameter. In most cases, it is recommended to set the **Attraction** and **Repulsion** parameters to values of 2 and 1, respectively. Values of 2 and 0 or 1 and 0 may also yield a good layout.

#### Advanced parameters

![Advanced layout parameters](/docs/assets/images/advanced_parameters_layout.png)

In general, it is recommended not to change the values of the advanced parameters of the layout technique used by VOSviewer Online.

#### Update layout

![Update layout button](/docs/assets/images/update_layout.png)

Use the **Update layout** button to update the layout of a network.

### Clustering

#### Resolution

![Resolution text field](/docs/assets/images/resolution.png)

The **Resolution** parameter determines the level of detail of the clustering of a network. The parameter must have a non-negative value. The higher the value of the parameter, the larger the number of clusters in the clustering of a network. It is recommended to try out different values for the **Resolution** parameter and to use the value that yields the most useful clustering.

#### Minimum cluster size

![Minimum cluster size text field](/docs/assets/images/minimum_cluster_size.png)

The **Minimum cluster size** parameter determines the minimum size of a cluster in the clustering of a network. Each cluster should include at least the minimum number of items specified by this parameter.

#### Merge small clusters

![Merge small clusters switch](/docs/assets/images/merge_small_clusters.png)

The **Merge small clusters** switch determines how small clusters, which do not include the minimum number of items specified by the **Minimum cluster size** parameter, are handled. If the switch is turned on, small clusters are merged into larger clusters. Otherwise small clusters are discarded.

#### Advanced parameters

![Advanced clustering parameters](/docs/assets/images/advanced_parameters_clustering.png)

In general, it is recommended not to change the values of the advanced parameters of the clustering technique used by VOSviewer Online.

#### Update clustering

![Update clustering button](/docs/assets/images/update_clustering.png)

Use the **Update clustering** button to update the clustering of a network.
