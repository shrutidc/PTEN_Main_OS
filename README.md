# Smart Pad Layout Optimizer

Develop a web application that uses real-world drone imagery to create intelligent pad layouts for hydraulic fracturing operations. The app should enable operators to optimize equipment placement while maintaining safety zones and operational efficiency.

## Core Requirements

### 1. Image Processing & Georeferencing

- **Input**: High-resolution drone imagery of completion pads
- **Coordinate Transformation**: Implement robust translation between image pixel coordinates and real-world GPS coordinates (lat/long)
- **Georeferencing Methods**: Support multiple approaches including:
  - Ground control points (GCPs) marked in the field
  - GPS metadata from drone imagery
  - Manual calibration using known reference points

### 2. Equipment Library & Placement

**Required Equipment Types:**
- Frac pumps (various horsepower ratings)
- Blenders and chemical additive units
- Sand storage and conveyor systems
- Data acquisition trailers
- Power generation units
- Support vehicles and crew areas
- Wireline equipment

**Features:**
- Drag-and-drop equipment placement interface
- Equipment-specific footprint dimensions
- Automatic orientation alignment options
- Collision detection between equipment

### 3. Safety & Operational Zones

**Customizable Zone Types:**
- Safety exclusion zones (personnel restrictions)
- Equipment operational clearances
- High-pressure line routing corridors
- Emergency evacuation paths
- Environmental buffer zones (if applicable)

**Zone Customization:**
- Color-coded zone types
- Overlap detection and warnings

### 4. Real-World Integration

- **GPS Coordinate Export**: Generate precise lat/long coordinates for each equipment piece
- **Change Detection**: Compare planned vs. actual layouts using follow-up drone imagery

## Technical Specifications

### Data Formats

- **Input**: JPEG/TIFF drone imagery with GPS metadata, GeoTIFF format preferred
- **Output**: KML/KMZ files, CSV coordinate lists, PDF layout reports

### Performance Targets

- Image processing: <10 seconds for imagery
- Real-time coordinate translation during equipment placement
- Support for pad images up to 50MB

### Programming

- This project will be a single-page web application built using **Angular** or **React**. 
- Back-end services are not required but maybe used.

## Provided Resources

- Sample drone imagery of actual completion pads are available in the `drone_scans` directory. Each example directory (e.g., `example-1`) contains:
  - `actual`: The actual layout of the pad once the equipment was moved to the job site. 
  - `plan`: The planned layout of the pad from an engineer for reference on how a job site is laid out.
  - `planning`: The planning image for the pad well before the job starts.
- Equipment specification sheets (dimensions, clearance requirements)
- GPS coordinates for sample images
- Mentorship from completion engineers

## Bonus Features

- AI-powered optimal layout suggestions
- 3D visualization capabilities