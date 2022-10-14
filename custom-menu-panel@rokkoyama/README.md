# Gnome Custom Menu Panel
Custom menu on Gnome Top Bar with your favorite program shortcuts.
License: GPL v3

This expands upon previous GPL works listed below in the predecessors section by adding:
- Expansion of Gnome compatibility to v43
- The ability to reload the configuration file, rebuild the menu and revalidate the configuration file JSON syntax without having to restart Gnome using the "Alt-F2, r" method or by logging in/out of the Gnome session.
- Added optional constants to the default configuration file (~/.entries)
	- 'editorExecutable', defaulted to 'gedit' (for Gnome < 42), 'gnome-text-editor' (for Gnome > 43) and
	- 'terminalExecutable', defaulted to 'gnome-terminal'.
	- These values are currently only used for the permanent 'Custom Menu Config' submenu items, where [Edit Config File] uses 'editorExecutable' and [View Log in Journalctl] uses 'terminalExecutable'.
	- The user remains able to specify their preferred text editor in the confiugration file to deviate from the default.
		- Tested custom values for 'editorExecutable' with Geany and 'terminalExecutable' with Tilix.
	- If a configuration file parsing error is detected, the appropriate text-editor is determined based on the Gnome Version.
	- As gnome-text-editor has replaced gedit in Gnome 43, the default text editor is now defined as a function of Gnome version being >= 43 or less than 43. The default text editor is used during generation of a default configuration file, as well as used as an editor to spawn when the configuration file parsing error is detected. 
- Added automatic expansion of the 'Custom Menu Config' submenu if ~/.entires JSON parsing fails.
---

GPL Predecessors (Newer to Older)

- https://github.com/andreabenini/gnome-plugin.custom-menu-panel (GPL v3)
- https://github.com/Shihira/gnome-extension-quicktoggler (GPL v2)
	- Deprecated - Author switched to developing for KDE.
