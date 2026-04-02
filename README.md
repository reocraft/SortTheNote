# The Sounds of Sorting

**Author:** Reo Saito

A Java GUI application that visualizes sorting algorithms and plays musical notes as they run. Each array element is mapped to a MIDI note — you can hear the structure of each algorithm as it sorts.

## Features

- **6 sorting algorithms:** Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, Quick Sort, and Event Sort
- **2 musical scales:** B Minor Pentatonic (17 notes) or Chromatic (36 notes)
- Real-time bar chart visualization at 20 FPS with color highlighting
- MIDI audio output via the built-in Java synthesizer

## Requirements

- Java 17+
- Maven

## Build & Run

```bash
mvn clean package
mvn exec:java
```

## Usage

1. Select a sorting algorithm from the **Sort** dropdown
2. Select a musical scale from the **Scale** dropdown
3. Click **Make Scale** to shuffle the array
4. Click **Play** to start the visualization

## Project Structure

```
src/main/java/edu/grinnell/csc207/soundsofsorting/
├── SortingVisualizer.java   # Entry point, creates the JFrame
├── ArrayPanel.java          # Bar chart visualization
├── ControlPanel.java        # Buttons and dropdowns
├── NoteIndices.java         # Shuffled array with highlight state
├── Scale.java               # MIDI note playback
├── sorts/
│   └── Sorts.java           # All 6 sorting algorithms
└── sortevents/
    ├── SortEvent.java        # Event interface
    ├── SwapEvent.java        # Records a swap
    ├── CompareEvent.java     # Records a comparison
    └── CopyEvent.java        # Records a copy (merge/insertion sort)
```

## Resources

- [Java AWT Graphics API](https://docs.oracle.com/javase/8/docs/api/java/awt/Graphics.html)
- [How to shuffle an ArrayList](https://stackoverflow.com/questions/16112515/how-to-shuffle-an-arraylist)
- [Maven MojoExecutionException](https://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException)
