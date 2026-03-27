# 🎓 Aetheria University Website

A modern, fully responsive university website built with vanilla HTML, CSS, and JavaScript — featuring multi-page navigation, an AI chatbot, global search, dark mode, and Supabase-powered application forms.

---

## 🌐 Live Demo

(https://ubiquitous-gaufre-1bd104.netlify.app/#)

---

## ✨ Features

- **Multi-Page SPA** — Home, About, Departments, Academics, Admissions, Placements, Research, Campus Life, Alumni, and Contact pages — all without a page reload.
- **Dark / Light Mode** — Toggle between themes with persistent styling.
- **AI Chatbot** — Keyword-aware assistant that answers common queries about admissions, fees, placements, hostels, and more.
- **Global Search** — `Ctrl+K` shortcut to search across all pages, departments, faculty, and sections.
- **Responsive Design** — Mobile-friendly with a hamburger menu and adaptive layouts.
- **Announcement Ticker** — Auto-scrolling banner for university news.
- **Supabase Integration** — Application form data is stored in a Supabase `applications` table.
- **Rich Sections** — Stats counters, testimonials, events calendar, faculty profiles, research centres, club listings, placement stats, alumni showcase, and more.

---

## 🛠️ Tech Stack

| Layer       | Technology                          |
|-------------|-------------------------------------|
| Markup      | HTML5                               |
| Styling     | CSS3 (Custom Properties / Tokens)   |
| Logic       | Vanilla JavaScript (ES6+)           |
| Fonts       | Google Fonts — Fraunces & DM Sans   |
| Backend     | [Supabase](https://supabase.com/)   |

---

## 📁 Project Structure

```
aetheria-university/
├── index.html       # Main (and only) HTML file — entire site lives here
└── README.md        # You're reading it!
```

---

## ⚙️ Setup & Configuration

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/aetheria-university.git
cd aetheria-university
```

### 2. Configure Supabase

In `index.html`, find the Supabase initialization block and replace the placeholder values with your own project credentials:

```js
const _supabase = supabase.createClient(
  'YOUR_SUPABASE_URL',
  'YOUR_SUPABASE_ANON_KEY'
);
```

> ⚠️ **Never commit real API keys to a public repository.** For production, use environment variables or a backend proxy.

### 3. Create the Supabase Table

In your Supabase dashboard, run the following SQL to create the `applications` table:

```sql
create table applications (
  id uuid default gen_random_uuid() primary key,
  name text,
  email text,
  program text,
  message text,
  created_at timestamp default now()
);
```

### 4. Run Locally

Since this is a single HTML file, simply open it in your browser:

```bash
# Option 1 — Just double-click index.html

# Option 2 — Use VS Code Live Server extension

# Option 3 — Use Python's built-in server
python3 -m http.server 8080
# Then open http://localhost:8080
```

---

## 🚀 Deployment

### GitHub Pages (Free & Easy)

1. Push code to GitHub (see guide below).
2. Go to your repo → **Settings** → **Pages**.
3. Under **Source**, select `main` branch and `/ (root)`.
4. Click **Save** — your site will be live at `https://YOUR_USERNAME.github.io/aetheria-university/`.

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
