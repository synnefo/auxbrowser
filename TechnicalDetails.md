# Technical Details #

## Security ##

Aux Browser puts the entire browser in a dedicated sandbox secured by system level technology.

This is different from Google Chrome which does not have system level sandbox(Reference: "Let the operating system apply its security ..." http://www.chromium.org/developers/design-documents/sandbox).

Also Aux browser puts the entire thing in sandbox, while Google Chrome does not put plugin in sandbox.(Reference: "Plugins have capabilities that aren't public standards, so we can't sandbox these yet." http://www.google.com/googlebooks/chrome/small_30.html). Aux Browser is able to to do this because we use system level sandbox.

Aux Browser empties the sandbox every time it starts. Let's do an experiment, set home page to "about:blank" inside sandbox, exit, and then run Aux Browser - the settings made inside sandbox are all lost. So, every time you start Aux Browser, it's a clean start(Here is a tip: to be absolutely secure, exit and then start, so it's a fresh browser session).

The malware problem is handled by sandbox. Another security problem is "phishing"(http://en.wikipedia.org/wiki/Phishing).

To solve "phishing", it's important to know the domain and protocol of web page. Aux Browser shows this information in a dedicated area, so users know exactly where the web page comes from. Simply move mouse over the "Go" button(the button on the left of address field), and this information is displayed.

## Convenience ##

Aux Browser always stays at system tray of Windows, and it's instantly available by clicking the ball icon in system tray. We don't mind if a few mega bytes of memory are used so browser can be instantly available when needed. However, is there any memory leak problem? Aux Browser puts each web page in different processes. When you click the close button, all web page processes are terminated, and memory used by previous web pages is all freed.

Aux Browser makes it really easy to access favorites - simply move mouse over the favorites button, and your latest favorites are displayed for you to click. You can also search your favorites by keyword. Google Chrome requires several clicks to do this, and the latest favorites are displayed at the end of list(scrolling required to get there), while Aux Browser only requires one action of moving mouse, and the latest favorites are displayed at the top of list.

With Aux Browser, accessing browser history is easy - simply move mouse over the address field, and your latest history is displayed for you to click. With Google Chrome, you need clicks in order to view history.

The menu of Aux Browser is designed so you can do what you want to do in the shortest possible time - "Save As", "Print" and "Open" are put in the first line; "Find", "Zoom In", "Zoom Out", and "Normal Size" are put in the second line, etc - it's all organized by category, and saves your time to click the intended item.

## Thanks ##

We express gratitude to the following people:
  * dross reported local zone bug.
  * neo reported Windows API buffer bug.

## Known Bugs That Are Not Fixed ##

We are working on the following problems:

  * Symptom: shut down Windows and sometimes Aux Browser displays error message.
  * Impact: while this does not effect security and convenience, it is a little annoying.
  * Workaround: click the close button on Aux Browser, and then shut down Windows.