# ConvComMoji

An extension of the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification that outlines possible use and application of emojis. It follows most of the original specification of Conventional Commits v1.0.0 defined [here](https://www.conventionalcommits.org/en/v1.0.0/#specification), but is more opinionated about what types should be used.

## Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt).

1. Commits MUST be prefixed with a type, which consists of a emoji, `✨`, `🐛`, etc., followed by the OPTIONAL scope, OPTIONAL `💥`, and REQUIRED terminal space.
1. The type `✨` MUST be used when a commit adds a new feature to your application or library.
1. The type `⚡️` MUST be used when a commit changes feature logic in your application or library while not being a fix.
1. The type `🔥` MUST be used when a commit removes feature from your application or library.
1. The type `🐛` MUST be used when a commit represents a bug fix for your application.
1. A scope MAY be provided after a type. A scope MUST consist of a noun describing a section of the codebase surrounded by parenthesis, e.g., `🐛(parser)`
1. A description MUST immediately follow the space after the type/scope prefix. The description is a short summary of the code changes, e.g., `🐛` array parsing issue when multiple spaces were contained in string.
1. A longer commit body MAY be provided after the short description, providing additional contextual information about the code changes. The body MUST begin one blank line after the description.
1. A commit body is free-form and MAY consist of any number of newline separated paragraphs.
1. One or more footers MAY be provided one blank line after the body. Each footer MUST consist of a word token, followed by either a `:<space>` or `<space>#` separator, followed by a string value (this is inspired by the git trailer convention).
1. A footer’s token MUST use `-` in place of whitespace characters, e.g., `Acked-by` (this helps differentiate the footer section from a multi-paragraph body).
1. A footer’s value MAY contain spaces and newlines, and parsing MUST terminate when the next valid footer token/separator pair is observed.
1. Breaking changes MUST be indicated in the type/scope prefix of a commit, or as an entry in the footer.
1. If included as a footer, a breaking change MUST consist of the emoji `💥`, followed by a colon, space, and description, e.g., `💥`: environment variables now take precedence over config files.
1. If included in the type/scope prefix, breaking changes MUST be indicated by a `💥` immediately before the `<space>`. In this case commit description SHALL be used to describe the breaking change and footer about breaking changes MAY be ommitted.
1. The units of information that make up Conventional Commits MUST NOT be treated as case sensitive by implementors.
1. List below contains emojis that MUST be used for their types. Additional types MAY be used, but there SHALL NOT be types with overlapping meaning where one is subset of the other e.g. `refactor ♻️` & `architecture refactor 🏗️` or `fix 🐛` & `critical fix 🚑`.

-   feature: ✨
-   update: ⚡️(to discuss)
-   remove: 🔥 (to discuss)
-   fix: 🐛
-   build: 📦
-   chore: 🔧
-   ci: 💚
-   docs: 📝
-   ui: 💎/💄 (to discuss)
-   style: 🎨
-   refactor: ♻️
-   performance: ⌛/🚀
-   test: 🧪
-   version tag: 🔖

-   revert: ⏪️
-   merge: 🔀
-   begin: 🎉
-   breaking change: 💥
-   wip: 🚧 - in specification it should be special case same as breaking change, warning to not interact with this branch/commit

If you are looking for more detailed description of changes made with commits you should check out [gitmoji](https://gitmoji.dev)
