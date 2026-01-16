Disclaimer:
If you are using this repository and pushing it to your own GitHub account, please ensure that your repository is set to private.
Keeping the repository public may unintentionally expose your images and other sensitive assets.



# ��� Birthday Countdown Website

Beautiful birthday website with countdown, photo gallery, and celebration effects!

---

## ��� Quick Start

```bash
npm install
npm run dev
```
Open `http://localhost:5173`

---

## ✏️ Customize

### 1. Birthday Date ⏰

**File:** `src/components/Countdown.jsx` (Line 21)

```javascript
const targetDate = new Date("2026-01-17T00:00:00");
```

**Format Explanation:**
```
"YYYY-MM-DDTHH:MM:SS"
 ↓    ↓  ↓  ↓  ↓  ↓
 Year Mo Day Hr Min Sec
```

- **YYYY** = 4-digit year (2025, 2026, etc.)
- **MM** = 2-digit month (01=Jan, 02=Feb, ... 12=Dec)
- **DD** = 2-digit day (01 to 31)
- **T** = Separator (keep this!)
- **HH:MM:SS** = Time in 24-hour format

**Time Examples:**
| What you want | Use this |
|---------------|----------|
| Midnight (12:00 AM) | `00:00:00` |
| 9:00 AM | `09:00:00` |
| Noon (12:00 PM) | `12:00:00` |
| 3:30 PM | `15:30:00` |
| 11:59 PM | `23:59:00` |

**Real Examples:**
```javascript
// January 15, 2026 at midnight
const targetDate = new Date("2026-01-15T00:00:00");

// June 10, 2025 at 3:30 PM
const targetDate = new Date("2025-06-10T15:30:00");

// December 25, 2025 at noon
const targetDate = new Date("2025-12-25T12:00:00");
```

**⚠️ Common Mistakes:**
- ❌ `2025-1-5` → ✅ `2025-01-05` (always 2 digits)
- ❌ `2025/12/25` → ✅ `2025-12-25` (use dashes, not slashes)
- ❌ Missing T → ✅ Must have `T` between date and time

---

### 2. Names & Message

**File:** `src/components/MessageCard.jsx` (Lines 17-28)

```javascript
const recipientName = "Kareena";
const senderName = "Yash";
const message = ``Dear Kareena, I won't promise I will move mountains for you or bring the moon down, but I would wake up in the middle of the night to make aglio olio just to see you smile and even pronounce it right, if I go wrong with the first 100 pictures I click, I will click a 100 more until you find your perfect one, but to me every picture is perfect, just how you make my life by simply being in it. Happy birthday, my love
```

---

### 3. Photos

Add 6 photos to `public/images/` named: `pic1.jpg` to `pic6.jpg`

---

### 4. Music (Optional)

Replace `public/music.mp3` with your song

---



**Why use it:**
- Test your message for typos
- Check if all 6 photos load correctly
- Verify music plays
- See confetti and animations
- Make sure everything looks perfect

---



---

### Clear Browser Storage (If Countdown Gets Stuck)

After testing with the test button, the countdown might stay on the celebration page even after refreshing. Here's how to reset it:

**Step-by-step instructions:**

1. **Open Developer Tools:**
   - Press `F12` on your keyboard
   - OR right-click anywhere on the page → click "Inspect"

2. **Go to Storage Area:**
   - Click the **"Application"** tab (Chrome/Edge)
   - OR click **"Storage"** tab (Firefox)

3. **Find Local Storage:**
   - In the left sidebar, look for "Local Storage"
   - Click the ▶ arrow to expand it
   - Click on `http://localhost:5173`

4. **Delete the Data:**
   - You'll see a row with key: `birthdayReached`
   - Right-click on it
   - Click "Delete"

5. **Refresh the Page:**
   - Press `Ctrl + R` (or `Cmd + R` on Mac)
   - The countdown should appear again!

**Visual Guide:**
```
Developer Tools (F12)
    ↓
Application/Storage Tab
    ↓
Local Storage → http://localhost:5173
    ↓
Right-click "birthdayReached" → Delete
    ↓
Refresh page (Ctrl + R)
```
<img width="1919" height="868" alt="image" src="https://github.com/user-attachments/assets/f0e3e12d-0b69-4a15-a571-7577594e0b5d" />

**When to do this:**
- After clicking the test button and wanting to see the countdown again
- If the celebration page won't go back to countdown
- When testing multiple times during development

---

## ��� Deploy

**Before going live:** Delete test button from `Countdown.jsx` (lines 95-101)

### Vercel
1. Push to GitHub
2. [vercel.com](https://vercel.com) → Import → Deploy

### Netlify
1. `npm run build`
2. [netlify.com](https://netlify.com) → Drag `dist` folder

---

## ��� Issues?

- **Photos not showing?** Check names (`pic1.jpg`) and location (`public/images/`)
- **Music not playing?** Named `music.mp3` in `public/` folder, MP3 format only
- **Countdown stuck?** See "Clear Browser Storage" section above

---

**Made with ❤️**
