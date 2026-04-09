# 📝 Notes App

A lightweight Android note-taking app built entirely in Jetpack Compose with SQLite for persistent local storage. 💾✨

---

## 🚀 Features

- ➕ Add, ✏️ edit, 🗑️ delete notes  
- 🔍 Search notes by title or description in real-time  
- 🌟 Mark notes as **Important**  
- 🎨 Material3 UI with Compose components  
- 🗄️ Uses `SQLiteOpenHelper` for local database management  

---

## 🧱 Architecture

- **UI:** Jetpack Compose (single activity + composables) 🖥️  
- **Database:** SQLite via `SQLiteOpenHelper` 🛠️  
- **State Management:** `remember` + mutable states for UI reactivity 🔄  

---

## 🗃️ Database Schema

| Column      | Type    | Description               |
| ----------- | ------- | ------------------------- |
| id          | INTEGER | Primary key (auto-increment) 🆔 |
| title       | TEXT    | Note title 🏷️            |
| description | TEXT    | Note body text 📝         |
| status      | TEXT    | Note status (`pending` or `Important`) ⭐ |

---

## 🧭 How to Use

- **Add Note:** Tap the "+" floating action button and fill in title/description. ➕  
- **Edit Note:** Tap the ✏️ edit icon on a note card to modify.  
- **Delete Note:** Tap the 🗑️ delete button on a note card.  
- **Mark Important:** Tap "Mark as Important" button on a note. 🌟  
- **Search:** Use the 🔍 search bar in the top app bar to filter notes by title or description.

---

## 🔍 Code Highlights

- `TaskDatabaseHelper` handles SQLite database creation and upgrades. 🛠️  
- `TaskManagerScreen` manages UI state and data flow. 🔄  
- Dialogs handle adding and editing notes with state hoisting. 🗣️  
- `LazyColumn` displays scrollable note list efficiently. 📃  

---

## 👀 Preview

Use Android Studio's Compose preview to visualize the UI via:

```kotlin
@Preview(showBackground = true)
@Composable
fun TaskManagerPreview() {
    MyApplicationTheme {
        TaskManagerScreen()
}
}
```
---

## 🔮 Future Improvements
🕒 Add timestamps and reminder notifications

☁️ Sync notes to cloud storage

🏷️ Add categorization/tags

🎬 Improve UI with animations and gestures

