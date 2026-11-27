
Error: Windows npm found in WSL

You're running Claude Code in WSL but using the Windows npm installation from /mnt/c/, which can't be updated.

To fix this:
  1. Install Node.js within your Linux distribution: e.g. sudo apt install nodejs npm
  2. Make sure Linux npm is in your PATH before the Windows version
  3. Try updating again with 'claude update'
