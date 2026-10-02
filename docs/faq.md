# FAQ

### Is Locply open source?

No. Locply is proprietary / closed source. This public repo hosts docs and feedback only.

### Is my data uploaded?

Product design is local-first: analysis is meant to stay on your device via **SQLite WASM** and browser storage. See the current privacy terms at [https://www.locply.com/legal/](https://www.locply.com/legal/).

### What database does Locply use?

SQL runs in the browser with **SQLite WASM**. When supported, Locply prefers OPFS for durable local files; otherwise it may fall back to less durable in-browser modes. Metadata uses IndexedDB-style local storage.

### Will clearing my browser wipe my workspace?

Yes, it can. Clearing site data, resetting the profile, or using private browsing can remove local workspaces. Export important data yourself.

### Where do I report bugs?

Open an Issue in this repository. Include browser, OS, version, and steps to reproduce.

### Can I contribute code?

Not to this product’s private source tree via this repo. Feedback and issue reports are welcome.
