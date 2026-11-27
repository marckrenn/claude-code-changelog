

Web pages can only be fetched through the ${…} agent in this session (there is no direct ${…} tool), so while this hook blocks it there is no other way to fetch them. If the page is required, tell the user; a hook that means to allow web fetching can exempt tool_input.subagent_type == "${…}" — a name match, which a project, user, or plugin agent defined under that same name would also pass with whatever tools it declares, so it fits only where no such agent is defined.
