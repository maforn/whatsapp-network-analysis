# WhatsApp Chat Network Analysis

This repository contains a Jupyter notebook that demonstrates how to parse a text-exported chat log, build a directed “message-response” graph, apply community detection (Louvain method), compute centrality metrics, and visualize both the network structure and community statistics.

## Features

- **Message parsing**  
  Read and clean raw chat text (Apple/Android exports) into structured message records.

- **Graph construction**  
  Build a directed NetworkX graph where nodes are participants and edges represent replies.

- **Community detection**  
  Use the Louvain algorithm to identify communities of tightly-interacting users.

- **Centrality analysis**  
  Compute degree, betweenness, and closeness centralities for each participant.

- **Visualization**  
  • Plot centrality distributions & community‐size histograms  
  • Render the message-response network with communities highlighted

## Requirements

- Python 3.7 or higher  
- Install dependencies with:

  ```bash
  pip install -r requirements.txt
  ```

## Usage

1. **Clone this repo**  
   ```bash
   git clone https://github.com/maforn/whatsapp-network-analysis.git
   cd whatsapp-network-analysis
   ```

2. **Add your chat file**  
   Place your exported chat text (e.g. `main.txt`) under `data/`.  
   The notebook expects it at `data/main.txt`.

3. **Launch the notebook**  
   ```bash
   jupyter notebook notebook.ipynb
   ```

4. **Run cells step by step**  
   - Parse messages  
   - Build and analyze the graph  
   - Experiment with different centrality measures or community-detection parameters  
   - Customize plots as desired

## Customization

- To analyze a different chat, update `FILE_PATH` in the first code cell to point to your file.
- Change the analysis function based on the export device (Android/IOS).
- Tweak the Louvain resolution parameter in the “Building the message-response graph” section.
- Add or remove centrality measures by modifying the analysis cells.

## Contributing

Contributions and suggestions are welcome! Feel free to open an issue or submit a pull request.

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.
