---
rank: 3
---
Under the hood, make.md runs as an engine that both keeps your information organized as well as turns the information into visualizations and workflows. This note goes into some of the architectural aspects of how make.md is designed for those interested.

---
### Superstate

The superstate is how information in your vault is kept connected and ensures quick access to information during runtime. When you start make.md, the superstate initiates and indexes all the files and notes you need for your workspace. As you work in your system, the superstate reacts and updates its connections so that links are automatically updated. The cached superstate is stored so that when you launch your vault again, the index loads immediately.
### Paths and Spaces

Everything in make.md is represented as an unique path. For example, when working in Obsidian, that path is the relative path from your vault root. Notes, folders, tags, tables, views and blocks all have their individual paths so that they can be linked from another part of your vault. The superstate reads through all your paths and keeps track of which paths are connected to other paths, which spaces they are in and etc. Spaces, contexts and views also keep track of their own information, for example, commonly used views are cached so they can render as soon as you open them. 
### Contexts

Contexts are SQLite database files for each of your folder or tag that stores the schema and data for each of your folders. Each context is stored with the folder under the .space config folder. When you make edits to the data or add additional items to the folder, your context database is automatically updated. 
### Views

In order to make sure that you are able to customize your workspace without any code, make.md comes with its own view compositor system. Each folder or tag comes with a main view which is defined by a series of subviews called frames. Each frame can be a context view, a note view, an image, a group or another predefined frame. There are a set of predefined frames that are built to compose your views quickly such as buttons, cards, tabs, list view items and more.

---
### Data Storage

Make.md stores configurations for spaces, contexts and views inside of the .space folder of each folder. These files are not created by default so only the folders you customize will contain these folders. For markdown files, properties are stored directly in the frontmatter of the file while for non-markdown files, it's stored inside the context database file.