${…} requires a git source, but no GitHub remote was detected${…}. The remote origin, ${…}, names the host "${…}", which a cloud session can't start from.
If "${…}" comes from your SSH configuration, replace HOST below with your git server's real host name, such as github.com, run the two commands, and start again. Git in this checkout will keep connecting through "${…}".
  git config url.${…}.insteadOf https://HOST/${…}/ && git remote set-url origin https://HOST/${…}/${…}
