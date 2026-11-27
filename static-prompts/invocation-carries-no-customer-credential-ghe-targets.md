${…}# Routes gh-to-github.com through the session relay ONLY when the
# invocation carries no customer credential. GHE targets (GH_HOST,
# --hostname, a -R/--repo/GH_REPO naming a non-github.com host, or a
# non-github.com origin remote in the cwd checkout) and
# real-customer-token invocations exec directly on the
# customer's own egress, so customer credentials never transit the
# relay tunnel and gh-to-GHE keeps working.
# Real customer tokens decide alone, checked first (costs nothing):
# gh sends GH_TOKEN/GITHUB_TOKEN proactively, and the GHE-scoped
# enterprise pair means gh may target a GHE host in ways the checks
# below cannot see (e.g. a URL positional arg) — never route any of
# them through the tunnel.
${…}${…}# NO_PROXY cleared: an ambient runner-host NO_PROXY covering
# github.com would make gh skip the relay and send the literal dummy
# token to the real GitHub API (hard 401).
${…}NO_PROXY='' no_proxy='' \
SSL_CERT_FILE='${…}' \
GH_TOKEN='${…}' GITHUB_TOKEN='${…}' \
exec '${…}' "$@"
