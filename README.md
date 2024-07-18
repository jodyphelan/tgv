# transmission-graph-viewer

This repository holds the code for a web-based viewer for transmission graphs. The viewer is written in JavaScript and uses the [cytoscape.js](https://js.cytoscape.org/) library to visualise the graph.

This viewer is designed to work with the a specific subset of JSON format with the following structure:

```json
{
  "nodes": [
    {
      "id": "node1",
      "properties": {}
    },
    {
      "id": "node2",
      "properties": {}
    }
  ],
  "edges": [
    {
      "source": "node1",
      "target": "node2",
      "properties": {}
    }
  ]
}
```

The properties field in the nodes and edges objects is optional and can be used to store additional information about the node or edge. The viewer will display this information in a tooltip when the user hovers over a node or edge. This format can be generated on the command-line by [tgtools](https://github.com/jodyphelan/tgtools).

## Usage

To use the viewer, simply navigate to [https://jodyphelan.github.io/tgv/](https://jodyphelan.github.io/tgv/) in a web browser. You will then be able to drop your json file and view the graph. 

## Examples

Two example graphs are provided in the [examples](examples) directory. These graphs can be viewed by downloading the .json files and dropping them into the viewer. Additional metadata is provided via CSV files that can also be downloaded and viewed by dropping them into the viewer.

## Self hosting

If you would like to host the viewer yourself, you can clone this repository and serve the files using a web server. For example, you can use the following commands to clone the repository and start a simple web server using Python:

```bash
git clone https://github.com/jodyphelan/tgv.git
cd tgv
python3 -m http.server
```

You can then navigate to [http://localhost:8000/](http://localhost:8000/) in a web browser to view the viewer.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
