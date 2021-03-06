---
layout: page
title: RML Data Display Elements
parent: rml
next: templates
---

### \<datagrid\>

`<datagrid>`{:.tag} represents an element capable of fetching, positioning and rendering dynamic tabulated data. For a detailed description see [Data grid]({{"pages/cpp_manual/element_packages/data_grid.html"|relative_url}}) in the C++ Manual.

_Attributes_

`source`{:.attr} = datasource (CS)
: The name of the data source and table that the rows of the data grid will be fetched from.

#### \<col\>

The `<col>`{:.tag} element represents a column in the datagrid. Each column displays information about each row in the data source in the form of one or more fields.

_Attributes_

`fields`{:.attr}  = cdata (CS)
: A comma-separated list of fields that this column will fetch from the data source about each row and display.

`formatter`{:.attr} = cdata (CS)
: The name of the data formatter to use to turn the raw field information into RML. If not set (or the formatter can't be found) then the raw text will be displayed.

`width`{:.attr} = number (CN)
: The width (in px or %) of the column.

### \<dataselect\>

The `<dataselect>`{:.tag} element is described in the [Forms](forms.html#dataselect) section.

### \<progressbar\>

The `<progressbar>`{:.tag} element can visually display progress or relative values. For a detailed description see [progress bar]({{"pages/cpp_manual/element_packages/progress_bar.html"|relative_url}}) in the C++ Manual.

_Attributes_

`value`{:.attr} = number (CN)
: A number [0, 1] representing the fraction of the progress bar that is filled and where 1 means completely filled.

`direction`{:.attr} = cdata (CI)
: The direction the progress bar expands with increasing values. Must be one of:
* `top`{:.value}
* `right`{:.value} (default)
* `bottom`{:.value}
* `left`{:.value}
* `clockwise`{:.value}
* `counter-clockwise`{:.value}

`start-edge`{:.attr} = cdata (CI)
: Only applies to `clockwise`{:.value} or `counter-clockwise`{:.value} directions. Defines which edge the
circle should start expanding from. Must be one of:
* `top`{:.value} (default)
* `right`{:.value}
* `bottom`{:.value}
* `left`{:.value}
