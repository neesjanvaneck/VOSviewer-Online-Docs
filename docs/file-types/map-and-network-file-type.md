# VOSviewer map and network files

VOSviewer map and network files are tab-delimited text files for storing a network. A map file contains information about the items in a network. A network file contains information about the links between items.

Map and network files have multiple columns, separated by a tab or alternatively by a comma or semicolon. Viewing and editing these files can best be done using spreadsheet software such as MS Excel.

## VOSviewer map files

A VOSviewer map file contains information about the items in a network. Items are characterized by attributes. Each column in a map file corresponds with an attribute. Except for the first line, each line in a map file corresponds with an item. The first line is a header line that designates for each column the attribute represented by that column.

A map file may include the following columns:

Header | Description
------ | -----------
id | ID of an item.
label | Label of an item.
description | Description of an item. A description may include HTML formatting.
url | URL of an item.
x | Horizontal coordinate of an item.
y | Vertical coordinate of an item.
cluster | Cluster to which an item belongs. A cluster is represented by an integer between 1 and 1000.
weight<...> | Weight of an item. A weight is a non-negative number.
score<...> | Score of an item.

If the label of an item contains a comma or semicolon, the label needs to be enclosed within double quotes. The same applies to the description of an item.

A map file may include multiple `weight<...>` columns. In the header of a `weight<...>` column, `...` needs to be replaced by a label. For example, a map file may include a `weight<Links>` column, a `weight<Documents>` column, and a `weight<Citations>` column. In the same way, a map file may include multiple `score<...>` columns.

## VOSviewer network files

A VOSviewer network file contains information about the links between items in a network. Each line in a network file corresponds with a link. A network file has two or three columns. The first two columns contain the IDs of pairs of items that are connected by a link. The third column contains the strength of a link, indicated by a positive number. If there are only two columns, all links have a strength of 1.

If a network file contains multiple links between the same pair of items, VOSviewer Online will merge these links into a single combined link. The strength of the combined link will be equal to the sum of the strengths of the individual links.

## Example

This is an example of a VOSviewer map file:

```
--8<-- "docs/assets/data/example_map.txt"
```

The above map file can be downloaded [here](/docs/assets/data/example_map.txt).

This is an example of a VOSviewer network file:

```
--8<-- "docs/assets/data/example_network.txt"
```

The above network file can be downloaded [here](/docs/assets/data/example_network.txt).

Providing the map and network file as input to VOSviewer Online yields the following visualization:

<iframe allowfullscreen="true" src="https://app.vosviewer.com/?map=https://app.vosviewer.com/docs/assets/data/example_map.txt&network=https://app.vosviewer.com/docs/assets/data/example_network.txt&simple_ui=true" width="100%" height="75%" style="border: 1px solid #ddd; max-width: 1200px; min-height: 500px"></iframe>
