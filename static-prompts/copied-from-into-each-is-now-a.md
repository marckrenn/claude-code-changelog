Copied ${…} ${…} from ${…} into ${…} — each is now a separate asset of the destination (new id, same bytes), independent of the source from here on:
${…}${…}
Reference a copy from the destination's page by its url verbatim — e.g. <img src=${…}> — never by the source's id, which resolves only on the source artifact. Everyone who can open the destination can load these; they stay until deleted with ${…}.
