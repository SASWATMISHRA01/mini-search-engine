# 🔎 Mini Search Engine

A simple **Java-based Mini Search Engine** that allows users to search for words across multiple indexed documents.

This project demonstrates how fundamental **Data Structures** can be used to build the core concept of a search engine. It uses **HashMap for document indexing** and a **Trie for word storage**, with a clean **Java Swing GUI** for interaction.

---

## ✨ Features

- 🔍 Search words across multiple documents
- ⚡ Fast word lookup using HashMap indexing
- 🌳 Trie-based word storage
- 📄 View all indexed documents
- 📊 Display document statistics
- 🖥️ Clean Java Swing graphical interface
- ❌ Displays a message when no matching document is found
- 🔢 Shows the number of matching documents
- 🎨 Custom rounded UI components and dark theme

The GUI includes a search bar, document/index statistics, result cards, and an option to view all indexed documents. 

---

## 🧠 DSA Concepts Used

### 1. HashMap

A `HashMap<String, ArrayList<Integer>>` is used as an inverted index.

```text
Word → Document IDs
```

Example:

```text
java → [1, 10]
data → [0, 3, 5]
```

This allows the application to quickly identify which documents contain a searched word.

### 2. Trie

A Trie is used to store indexed words character by character.

```text
        root
         |
         d
         |
         a
        / \
       t   y
       |
       a
       |
       ...
```

Each Trie node contains its child characters and an `isEnd` flag to identify complete words.

---

## ⚙️ How It Works

```text
             ┌──────────────────┐
             │   Add Document   │
             └────────┬─────────┘
                      ↓
             ┌──────────────────┐
             │  Process Words   │
             └────────┬─────────┘
                      ↓
            ┌─────────┴─────────┐
            ↓                   ↓
      ┌───────────┐       ┌───────────┐
      │  HashMap  │       │    Trie   │
      │   Index   │       │   Store   │
      └─────┬─────┘       └───────────┘
            ↓
      ┌──────────────┐
      │ User Search  │
      └──────┬───────┘
             ↓
      ┌──────────────┐
      │ Search Index │
      └──────┬───────┘
             ↓
      ┌──────────────┐
      │ Show Results │
      └──────────────┘
```

When a document is added:

1. The document is assigned an ID.
2. Text is converted to lowercase.
3. Special characters are removed.
4. The document is split into individual words.
5. Each word is added to the HashMap index.
6. Each word is inserted into the Trie.

When a user searches:

1. The query is converted to lowercase.
2. The HashMap is checked for the word.
3. Matching document IDs are retrieved.
4. Matching documents are displayed in the GUI.

---

## 🖥️ User Interface

The application is built using **Java Swing** and uses a dark-themed interface with:

- Search bar
- Search button
- Document statistics
- Indexed word count
- Search results
- No-result state
- View All Documents window

The main window is designed around a simple search experience.

---

## 📚 Sample Documents

The application comes with **20 sample documents** covering topics such as:

- Data Structures
- Algorithms
- Java
- Web Development
- C++
- Machine Learning
- DBMS
- Operating Systems
- Computer Networks
- Artificial Intelligence
- Cloud Computing
- Cyber Security
- Python
- JavaScript
- Computer Architecture
- Theory of Computation
- Compiler Design
- Mobile Application Development
- Full Stack Development

These documents are loaded when the application starts.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java | Core programming |
| Java Swing | Graphical User Interface |
| HashMap | Document indexing |
| Trie | Word storage |
| ArrayList | Document and result storage |
| Data Structures | Search and indexing logic |

---

## 📁 Project Structure

```text
Mini-Search-Engine/
│
├── main.java
├── SearchEngineGUI.java
│
├── Main.class
├── MiniSearchEngine.class
├── SearchEngineGUI.class
├── TrieNode.class
│
└── README.md
```

The main search logic is implemented in `MiniSearchEngine`, while `SearchEngineGUI` handles the graphical interface.

---

## 🚀 How to Run

### Prerequisites

Make sure Java is installed:

```bash
java --version
javac --version
```

### Compile

```bash
javac main.java SearchEngineGUI.java
```

### Run

```bash
java Main
```

> **Note:** The exact compile command may depend on how the Java source files are organized in your local project.

---

## 🔍 Example Searches

Try searching for:

```text
java
data
machine
learning
python
network
web
security
```

For example:

```text
Search: java
```

The application returns the documents containing the searched word.

---

## 🎯 Learning Objectives

This project was created to understand:

- How search engines maintain an index
- How HashMap can be used for fast lookup
- How Trie data structures work
- Document indexing
- Searching algorithms
- Java Swing GUI development
- Connecting DSA logic with a real application

---

## 🔮 Future Improvements

Possible improvements include:

- [ ] Prefix/autocomplete search using Trie
- [ ] Search suggestions
- [ ] Multi-word search
- [ ] Search ranking
- [ ] TF-IDF based ranking
- [ ] Document upload functionality
- [ ] Search history
- [ ] Highlight matched words
- [ ] Persistent document storage
- [ ] Support for larger document collections

---

## 👨‍💻 Project

**Mini Search Engine**

Built with **Java + Data Structures + Java Swing**

> A small project demonstrating how fundamental DSA concepts can be used to build the core functionality of a search engine.
└── README.md
