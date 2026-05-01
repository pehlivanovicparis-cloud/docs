# 🌍 World Digital Clock

A real-time digital clock displaying the current time across multiple time zones with an interactive, responsive UI.

## Features

✨ **Multi-Timezone Display**
- Displays 6 major time zones by default (New York, London, Tokyo, Sydney, Dubai, São Paulo)
- Add or remove time zones on the fly
- 18 popular time zones to choose from

🔄 **Time Format Toggle**
- Switch between 12-hour (AM/PM) and 24-hour formats
- Instant format switching without page refresh

📊 **Rich Information**
- Real-time digital time display (updates every second)
- Current date for each timezone
- UTC offset for each location
- Last update timestamp

🎨 **Beautiful UI**
- Responsive grid layout (auto-adjusts from 1 to 3+ columns)
- Smooth hover animations
- Gradient background with card-based design
- Works perfectly on desktop, tablet, and mobile devices

🎮 **Interactive Controls**
- ➕ Add more time zones from available options
- ❌ Remove individual time zones
- ↺ Reset to default time zones
- 🔄 Toggle between time formats

## How to Use

### Online
1. Open `timezone-clock.html` in any modern web browser
2. Watch the time update in real-time across all time zones
3. Use the controls to customize your view

### Available Time Zones
- **Americas**: New York, Los Angeles, Chicago, Denver, Toronto, Mexico City, São Paulo
- **Europe**: London, Paris, Berlin
- **Asia**: Tokyo, Hong Kong, Singapore, Bangkok, Dubai, Mumbai
- **Australia**: Sydney

## File Structure

```
timezone-clock.html  - Complete standalone HTML file with embedded CSS and JavaScript
```

## Browser Support

✅ Works on all modern browsers:
- Chrome/Chromium
- Firefox
- Safari
- Edge

## Customization

You can easily customize the clock by editing the JavaScript section:

### Change Default Time Zones
Find this line and modify the array:
```javascript
let activeTimezones = ['New York', 'London', 'Tokyo', 'Sydney', 'Dubai', 'São Paulo'];
```

### Add New Time Zones
Add entries to the `TIMEZONES` object:
```javascript
const TIMEZONES = {
    'Your City': 'Continent/City',
    // ... more entries
};
```

### Modify Colors
Edit the CSS color values in the `<style>` section:
- `background: linear-gradient(...)` - Main background
- `.clock-card` - Card background and shadows
- `color: #667eea` - Primary accent color

### Change Update Frequency
Modify the interval (currently 1000ms = 1 second):
```javascript
setInterval(updateAllClocks, 1000);  // Change this number
```

## Technical Details

- **Pure HTML/CSS/JavaScript** - No dependencies or frameworks
- **Responsive Design** - CSS Grid for automatic layout adjustment
- **Real-time Updates** - JavaScript setInterval for continuous time updates
- **Timezone Handling** - Using browser's Intl API and `toLocaleString()` for accurate timezone conversion
- **Local State Management** - All preferences stored in JavaScript variables (refresh resets to defaults)

## Features Explained

### 12/24 Hour Format Toggle
- Default: 12-hour format (with AM/PM)
- Click "Toggle Format" button to switch
- Format applies to all time zones simultaneously

### Add Time Zones
- Click on any timezone button in the "Add More Time Zones" section
- Button becomes disabled once added
- Button re-enables if you remove that timezone

### Reset to Default
- Restores the original 6 time zones
- Helpful if you've added too many or want to start over

## Performance Notes

- Very lightweight and efficient
- Updates only DOM elements that need changing
- Smooth animations don't impact performance
- Works smoothly even on older devices

## Future Enhancements

Possible additions:
- ✨ Save preferred time zones to localStorage
- 🌙 Dark mode theme
- 🔔 Alarms/notifications for specific times
- 🌡️ Weather information
- 📍 Interactive world map with time zones
- ⚙️ Settings panel for customization

## License

This clock is part of the GitHub Docs repository and follows the same license.

---

**Created**: 2026-05-01
**Last Updated**: 2026-05-01
