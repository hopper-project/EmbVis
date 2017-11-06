# EmbVis

EmbVis is a tool for visualizing and browsing data object embeddings such as word embeddings and exponential family embeddings. 
It is written in JS and it uses the D3 library to display data points. It also allows for the search of object embeddings (e.g. words). 

(C) Copyright 2016, Kriste Krstovski kriste.krstovski@columbia.edu

This is free software, you can redistribute it and/or modify it under the terms of the GNU General Public License.

The GNU General Public License does not permit this software to be redistributed in proprietary programs.

This software is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

You should have received a copy of the GNU General Public License along with this program; if not, write to the Free Software Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307 USA


## How to Run

EmbVis requires a **data source file** that contains object names and their coordinates. The data source file is specified as a JS file within the embvis.html file:

\<script src="**data_source_file**.js"></script>

It should have the following format:

var objectpoints = [ 
{"title" : "data_object_title_to_be_displayed**","image" : "**image_file**",  "coord" : [**longitude_value**,**latitude_value**], "fill" : "**circle_fill_color**", "stroke" : "**stroke_fill_color**", "category" : "**category_type**"},
...
]

In the current implementation:

* The **image file** contains the path of the image file that is to be displayed when the user hovers over the data object point. 
* **circle_fill_color** is a decimal value between 0 and 1 and used to specify the fill color of the data point circle
* **stroke_fill_color** is the color name of the data point circle stroke (e.g. "red","blue", etc.) 
* **category_type** is used to specify the data object category (this value is currently not used)

Here is an example entry for the word "cosine" as a data object:

{"title": "cosine", "coord": [-11.7836261004,-26.4969584853], "fill": "0.8", "stroke": "blue", "category": "1"}

In this case we don't specify an image to be displayed for this data object. 

