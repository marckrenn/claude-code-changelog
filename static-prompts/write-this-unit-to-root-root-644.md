Write this unit to ${…}, root:root 644:
${…}
Before you enable it, add the SELF_HOSTED_AGENT_PROXY_* settings the proxy needs as Environment= lines, as the "Settings" section of ${…} lists them, and any hook and secret lines. As root, leave ${…} unset, so the proxy logs to the journal, or name a file in a folder only root can write, so never under /var/log on Ubuntu, whose group can write it. With hooks, set TimeoutStopSec to the hook timeout plus 15 seconds (the timeout defaults to ${…}s); without, keep 30.
