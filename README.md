# VibeML: A Personalized Spotify Playlist Generation Agent

VibeML is an LLM-based Spotify playlist agent that generates personalized song recommendations based on a user's mood, activity, vibe, and feedback.

## Project Goal

The goal of this project is to build a code-first AI agent that can map a user's request to music-related features, search Spotify-style datasets, recommend tester songs, collect feedback, and generate a final playlist.

## Repository Structure

* `docs/` - Project scope, acceptance criteria, and data setup notes
* `notebooks/` - Databricks notebooks for data pipeline, agent prototype, and evaluation traces
* `data/` - Placeholder folders for raw and processed data structure
* `src/` - Agent tools and supporting Python functions
* `outputs/` - Generated playlist outputs
* `traces/` - Evaluation traces and run outputs

## Data Setup

The full datasets are not stored directly in GitHub. The `data/raw` and `data/processed` folders are included for project organization only.

For the current Databricks workflow, the raw Kaggle datasets were uploaded into Databricks Catalog as:

* `main.default.spotify_tracks_raw`
* `main.default.spotify_data_clean_raw`
* `main.default.track_data_final_raw`

The processed MVP recommendation table created by the data pipeline notebook is:

* `main.default.vibeml_tracks_processed`

If another teammate runs the notebook in a different Databricks workspace, they will need to download the Kaggle CSV files, upload them into their own Databricks Catalog, and use the same table names above so the notebook runs without path changes.

## Planned Notebooks

* `01_data_pipeline` - Load, inspect, clean, and prepare Spotify datasets
* `02_agent_prototype` - Build the first version of the agent and tools
* `03_evaluation_traces` - Run test scenarios and document evaluation results

## Current MVP Scope

The MVP uses the Kaggle Spotify datasets as the main data foundation. Live Spotify API access is a stretch goal for now.


## AI Tool Disclosure
This project used AI tools in development. Databricks' built-in AI agent was used for generating portions of the code. Additional AI tools used by team members include ChatGPT, Claude, and Grok, applied to coding, animation creation, and presentation outlines.
