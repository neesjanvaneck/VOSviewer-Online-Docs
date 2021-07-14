# Embedding a visualization

A visualization of a network in VOSviewer Online can be shared by embedding the visualization in a webpage.

This is an example of HTML code for embedding a visualization in a webpage:

``` html
<iframe
  allowfullscreen="true"
  src="https://app.vosviewer.com/?json=https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.json&simple_ui=true"
  width="100%"
  height="75%"
  style="border: 1px solid #ddd; max-width: 1200px; min-height: 500px"
>
</iframe>
```

The `src` attribute in the HTML code provides a [link to a visualization](/docs/sharing/linking/). It is recommended to include the `simple_ui` parameter in this link and to set this parameter to `true`. Other parameters may be included in the link as well.

Using the above HTML code, the following visualization is obtained:

<iframe allowfullscreen="true" src="https://app.vosviewer.com/?json=https://app.vosviewer.com/data/QSS_SM_2020-2021_co-authorship_network.json&simple_ui=true" width="100%" height="75%" style="border: 1px solid #ddd; max-width: 1200px; min-height: 500px"></iframe>
