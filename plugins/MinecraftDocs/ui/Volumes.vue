<template>
<div style="overflow: scroll">
<v-html>
<h1>VOLUMES DOCUMENTATION </br>Version: 1.17.10.4</h1>
<h2><p id="Index">Index</p></h2>
<table border="1">
<tr> <th><a href="#Volumes">Volumes</a></th> </tr>
<tr> <td> <a href="#Volume Components"> Volume Components</a> </tr> </td>
<tr> <td> <a href="#Volume Definition Properties"> Volume Definition Properties</a> </tr> </td>
<tr> <td> <a href="#Volume Description Properties"> Volume Description Properties</a> </tr> </td>
</table>
<a href="#Index">Back to top</a>
<h1><p id="Volumes">Volumes</p></h1>

<h1><p id="Volume Components">Volume Components</p></h1>

These are the various possible components for this entity</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:bounds</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Component that defines a minimum and maximum block position for a bounding box and which world dimension the bounding box is in. Every volume must have a bounds component.</br><table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Default Value</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">dimension</td>
<td style="border-style:solid; border-width:2; padding:8px">String</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">The name of the dimension the bounding box will exist in: one of 'overworld', 'nether' or 'the end'.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">max</td>
<td style="border-style:solid; border-width:2; padding:8px">Vector [a, b, c]</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">The maximum block position of the bounding box.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">min</td>
<td style="border-style:solid; border-width:2; padding:8px">Vector [a, b, c]</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">The minimum block position of the bounding box.</br></td>
</tr>
</table>
</td>
</tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">minecraft:fog</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Displays the given fog whenever a player enters the volume. Each volume can only have one fog attached.</br><table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:2;">
<tr> <th style="border-style:solid; border-width:2;">Name</th> <th style="border-style:solid; border-width:2;">Type</th> <th style="border-style:solid; border-width:2;">Default Value</th> <th style="border-style:solid; border-width:2;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">fog_identifier</td>
<td style="border-style:solid; border-width:2; padding:8px">String</td>
<td style="border-style:solid; border-width:2; padding:8px"></td>
<td style="border-style:solid; border-width:2; padding:8px">The identifier of a fog definition. Note that you will not receive any feedback if the definition does not exist.</br></td>
</tr>
<tr>
<td style="border-style:solid; border-width:2; padding:8px">priority</td>
<td style="border-style:solid; border-width:2; padding:8px">Integer</td>
<td style="border-style:solid; border-width:2; padding:8px">INT_MAX</td>
<td style="border-style:solid; border-width:2; padding:8px">The priority for this fog definition setting. Smaller numbers have higher priority. Fogs with equal priority will be combined together.</br></td>
</tr>
</table>
</td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<h1><p id="Volume Definition Properties">Volume Definition Properties</p></h1>

The properties of a minecraft:volume entity. Note that every volume must have a bounds component. All other components are optional.</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">format_version</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">Specifies the version of the game this entity was made in. Minimum supported version is 1.17.0. Current supported version is 1.17.0.</br></td>
</tr>
</table>
<h2>Example</h2>
Example<br / ><textarea readonly="true" cols="58" rows="19">
{
  "format_version": 1.17.0,
  "minecraft:volume": {
    "description": {
      "identifier": "your_custom_namespace:sample_volume"
    },
    "components": {
      "minecraft:bounds": {
        "min": [-50, 0, -50],
        "max": [50, 256, 50]
      },
      "minecraft:fog": {
        "fog_identifier": "minecraft:fog_savanna",
        "priority": 1
      }
    }
  }
}
</textarea> </br>
<a href="#Index">Back to top</a><br><br>

<h1><p id="Volume Description Properties">Volume Description Properties</p></h1>

The description contains a single 'identifier' string</br><h2></h2>

<table border="1" style="width:100%; border-style:solid; border-collapse:collapse; border-width:3;">
<tr> <th style="border-style:solid; border-width:3;">Name</th> <th style="border-style:solid; border-width:3;">Type</th> <th style="border-style:solid; border-width:3;">Default Value</th> <th style="border-style:solid; border-width:3;">Description</th> </tr>
<tr>
<td style="border-style:solid; border-width:3; padding:7px">identifier</td>
<td style="border-style:solid; border-width:3; padding:7px">String</td>
<td style="border-style:solid; border-width:3; padding:7px"></td>
<td style="border-style:solid; border-width:3; padding:7px">The unique identifier for this volume. It must be of the form 'namespace:name', where namespace cannot be 'minecraft'.</br></td>
</tr>
</table>
<a href="#Index">Back to top</a><br><br>

<br><br>

</v-html>
</div>
</template>

<style scoped>
textarea{
  color: white;
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: white;
}

::-webkit-scrollbar-track {
  background: grey;
}
</style>