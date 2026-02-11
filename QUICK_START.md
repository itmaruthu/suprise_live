# Valentine's Website - Quick Start Guide 🎵💕

## What Happens When She Visits:

### ✅ BEFORE Countdown Ends:
1. **Random Love Quote** displays with romantic image
2. **Music starts playing** automatically (if browser allows)
3. **Countdown timer** shows time remaining
4. **Floating hearts** animate in background
5. **Music player** visible in bottom-right corner

### 🎉 AFTER Countdown Ends (or reaches zero):
1. **Celebration overlay** appears with confetti
2. She clicks "See My Surprise!"
3. **All content reveals**:
   - Love story
   - Your romantic poems
   - Photo gallery
   - Timeline of memories
   - Footer message
4. **Music continues playing** throughout

---

## 🎵 Step 1: Add Your Music (IMPORTANT!)

### Option A: Using Dropbox (Easiest)

1. Upload your MP3 to Dropbox
2. Get the share link
3. Change `www.dropbox.com` to `dl.dropboxusercontent.com`
4. Change `dl=0` to `dl=1` at the end

**Example:**
```
Original: https://www.dropbox.com/s/abc123/song.mp3?dl=0
Changed:  https://dl.dropboxusercontent.com/s/abc123/song.mp3?dl=1
```

5. Find this in the HTML (around line 377):
```javascript
const songURL = ""; // Add your song URL here
```

6. Paste your URL:
```javascript
const songURL = "https://dl.dropboxusercontent.com/s/abc123/song.mp3?dl=1";
```

7. Update song details:
```javascript
const songTitle = "Perfect";
const songArtist = "Ed Sheeran";
```

### Option B: Using Google Drive

1. Upload MP3 to Google Drive
2. Right-click → Share → Anyone with link
3. Copy the file ID from the link
4. Use: `https://drive.google.com/uc?export=download&id=YOUR_FILE_ID`

---

## ⏰ Step 2: Set Your Countdown Date

Find this in the HTML (around line 367):

### For Testing (2 minutes from now):
```javascript
const targetDate = new Date(Date.now() + 2 * 60 * 1000); // CURRENT SETTING
```

### For Valentine's Day 2026:
```javascript
const targetDate = new Date(2026, 1, 14, 0, 0, 0); // Feb 14, 2026 midnight
```

### For Another Date:
```javascript
const targetDate = new Date(2026, 5, 15, 19, 0, 0); // June 15, 2026 at 7:00 PM
// Format: (Year, Month-1, Day, Hour, Minute, Second)
// Months: Jan=0, Feb=1, Mar=2, Apr=3, May=4, Jun=5, Jul=6, Aug=7, Sep=8, Oct=9, Nov=10, Dec=11
```

---

## 📝 Step 3: Customize Your Content

### Update Poems:
Find the poems section and edit or add more:
```html
<div style="margin: 30px 0; padding: 30px; background: linear-gradient(135deg, #ffeef8 0%, #fff5f7 100%); border-left: 4px solid #d63384; border-radius: 10px;">
    <h3 style="color: #d63384; margin-bottom: 15px; font-size: 1.5em;">Your Poem Title</h3>
    <p style="font-size: 1.1em; line-height: 1.8; color: #555; font-style: italic; white-space: pre-line;">Your poem text here
Line breaks are preserved
Just write naturally</p>
</div>
```

### Update Photos:
Replace the image URLs in the photo gallery section:
```html
<img src="YOUR_PHOTO_URL_HERE" alt="Our Memory">
```

### Update Timeline Dates:
Find `[Add Your Date]` and replace with your actual dates.

---

## 🎨 Love Quotes Configuration

The website randomly shows one of 10 romantic quotes each time it's visited. These are already configured!

**Current quotes include:**
- "You are my today and all of my tomorrows." - Leo Christopher
- "In all the world, there is no heart for me like yours..." - Maya Angelou
- And 8 more beautiful quotes!

**To add your own quotes**, find this section (around line 205) and add to the array:
```javascript
{
    text: "Your custom quote here",
    author: "Author Name"
}
```

---

## 🚀 Testing Your Website

### Test Locally:
1. Save the HTML file
2. Double-click to open in browser
3. Music should try to auto-play (may need to click play button first)
4. Countdown will be running
5. When countdown ends → Celebration → Content reveals

### Quick Test (2 minute countdown):
The file is already set to 2 minutes for testing! Just open it and wait.

### Reset Test:
To test again, just refresh the page.

---

## 🎵 Music Player Features

**Controls:**
- ▶/⏸ - Play/Pause
- 🔊 - Click to mute/unmute
- Slider - Adjust volume
- Music loops automatically

**Auto-play:**
- Music tries to start automatically
- If blocked by browser, she just clicks the play button
- Music continues even after countdown ends

---

## 📱 Mobile Friendly

Everything works on phones and tablets:
- Countdown adjusts size
- Music player is responsive
- Photos stack properly
- All content is readable

---

## ✅ Final Checklist

Before giving to your wife:

- [ ] Added song URL
- [ ] Updated song title and artist
- [ ] Set correct countdown date
- [ ] Replaced placeholder photos
- [ ] Updated timeline dates
- [ ] Customized love story text
- [ ] Added/edited poems
- [ ] Tested on your browser
- [ ] Tested music plays
- [ ] Checked countdown works

---

## 🎁 What Makes This Special

1. **Random Quote** - Different romantic quote each visit
2. **Music** - Her favorite song playing
3. **Countdown** - Builds anticipation
4. **Celebration** - Confetti and animation when revealed
5. **Personal Content** - Your poems, photos, memories
6. **Beautiful Design** - Professional and romantic

---

## 🔧 Troubleshooting

**Music won't auto-play?**
- This is normal! Browsers block auto-play
- She just needs to click the play button once
- After that, it will continue playing

**Countdown not working?**
- Check the date format
- Make sure month is 0-indexed (Jan=0, Feb=1, etc.)
- Check JavaScript console for errors

**Photos not showing?**
- Make sure image URLs are direct links
- Test URL by pasting in browser
- Use HTTPS URLs, not HTTP

---

## 💝 You're All Set!

Your Valentine's website is ready to make her day unforgettable!

**What she'll experience:**
1. Opens page → Beautiful quote + romantic image + music
2. Sees countdown timer
3. Music playing in background
4. Waits for countdown (or you can set it to reveal immediately)
5. BOOM! Celebration + Confetti
6. All your love revealed: poems, photos, memories
7. Music continues throughout

**She's going to love this!** 🎵💕
