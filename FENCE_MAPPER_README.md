# Property Fence Mapper

A web application that allows you to search for a property address and draw fence sections on a high-resolution satellite map.

## Features

### 1. Address Search with Autocomplete
- Enter an address in the search box
- Auto-updating predictions appear as you type
- Select your desired address from the dropdown
- Selected address is displayed above the map
- Map automatically zooms to the property location

### 2. High-Resolution Satellite Map
- Satellite imagery at maximum zoom (21) for best resolution
- Overhead view (tilt: 0) ideal for property surveying
- Option to switch between satellite and hybrid views
- Map centered on selected property

### 3. Fence Drawing Tool
- Draw fence sections using straight lines
- Click on the map to add points and create line segments
- Multiple points create connected straight fence lines
- Each fence section can be completed and a new one started
- Visual feedback with red lines while drawing, blue when finished

## How to Use

### Setup
1. Open `property-fence-mapper.html` in a web browser
2. **Important**: Replace `YOUR_API_KEY_HERE` in the HTML file with your Google Maps API key
   - You need to enable both Maps JavaScript API and Places API in your Google Cloud Console

### Using the Application

1. **Search for Address**
   - Type the property address in the search box
   - Select the correct address from the autocomplete suggestions
   - The map will zoom to your property at maximum resolution

2. **Start Drawing Fence**
   - Click the "Start Drawing Fence" button
   - The button will turn green to indicate drawing mode is active

3. **Add Fence Points**
   - Click on the map to add points for your fence line
   - Each click creates a new point connected by a straight line
   - Red dots appear at each point you add
   - The fence line is shown in red while drawing

4. **Undo Points**
   - Click "Undo Last Point" to remove the most recent point
   - Available only while in drawing mode

5. **Finish a Fence Section**
   - Click "Finish Fence Section" when done with current section
   - The fence line will turn blue to indicate it's complete
   - You can start a new section by clicking "Start Drawing Fence" again

6. **Clear All Fences**
   - Click "Clear All Fences" to remove all fence sections
   - Confirmation dialog will appear before clearing

## Technical Details

- **Map Type**: Satellite with overhead view (tilt: 0)
- **Maximum Zoom**: Level 21 (highest resolution available)
- **Fence Line Color**: Red (while drawing), Blue (completed)
- **Drawing Method**: Straight line segments (geodesic: false for true straight lines)

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection
- Google Maps API key with Places API enabled

## File Structure

- `property-fence-mapper.html` - Main application file (standalone, no dependencies)

## Notes

- The application uses Google Maps JavaScript API and Places API
- Fence sections are drawn as polylines with straight segments
- All state is maintained in browser memory (no backend storage)
- Each fence section is independent and can be managed separately
