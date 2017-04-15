
Welcome to Intelephense! 

A high performance and feature rich PHP language server implemented in typescript. This extension offers:

* Fast fuzzy matching completion provider (Intellisense) offering suggestions found from within the workspace and from 11000+ built-in PHP symbols with associated documentation (PDO etc).
* Signature help for workspace and built-in constructors, methods, and functions.
* Go to definition support.
* Fast fuzzy workspace symbol search.
* Document symbol search.
* Parse error diagnostics for open files via an error tolerant parser that can report more than the first error encountered.

This extension is currently in beta. Additional features are under development. Your feedback, bug reports and help are appreciated and can be filed in the repository found HERE. The PHP parser used in the extension can be found HERE. 

Turn off vscode `php.suggest.basic` for best results. It is recomended to keep the vscode built-in php linter enabled as the Intelephense parser does not identify all compile time errors at present.

FAQ

How can I increase workspace symbol discovery time?
Intelephense workspace symbol discovery is fast, non-blocking and symbols become available as they are discovered.The total discovery time will depend on the number of files processed and the size of each file. Check the contents of your dependecies folder and add any files you do not need intelligence on to `files.exclude` to reduce total discovery time. Increasing `intelephense.workspaceDiscovery.maxOpenFiles` may also reduce discovery time.

How can I get intelligence on php files with a non-standard file extension?
Add your file extension to the vscode `files.associations` setting.

Can I adjust the frequency of diagnostics?
Yes. Adjust the `intelephense.diagnosticsProvider.debounce` setting. A higher number will reduce the frequency that diagnostics are published. 


