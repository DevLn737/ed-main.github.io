# Shikimori compatibility

Visual baseline: `Shikista` with `On Battle`. Secondary release palette: `Endless Horizon`.

Statuses: `mapped`, `patched`, `verified`, `limited`.

## shikimori.rip

| Area | Representative URL | Body page class | States/components | CSS scope | Status |
| --- | --- | --- | --- | --- | --- |
| Home | `/` | `p-dashboards p-dashboards-show` | catalog entries, news/topic previews, reviews, quotes, spoilers | shared `main_code_*` | mapped |
| Anime/manga/ranobe catalogs | `/animes`, `/mangas`, `/ranobe` | `p-animes_collection p-animes_collection-index` | pagination, catalog entries, collection filters, season/year/range selectors | shared `main_code_*` | mapped |
| VN catalog | `/visual_novels` | `p-animes_collection p-animes_collection-index` | `c-visual_novel`, VN navigation/list icons, filters | shared `main_code_*` | mapped |
| Anime/manga/ranobe entries | `/animes/52991-sousou-no-frieren`, `/mangas/4632-oyasumi-punpun`, `/ranobe/102875-fata-morgana-no-yakata-anata-no-genten-ni-itaru-monogatari` | `p-*-show p-db_entries p-db_entries-show p-animes p-animes-show` | poster actions, user rate, MAL/Shikimori scores, metadata, related entries, comments | shared `main_code_*` | mapped |
| VN entry | `/visual_novels/37866-of-the-devil` | `p-visual_novels p-visual_novels-show p-db_entries p-db_entries-show p-animes p-animes-show` | platform/genre tags, VN rate, screenshots, empty comments | shared `main_code_*` | mapped |
| Forum | `/forum`, `/forum/offtopic/5003548-spisok-izmeneniy` | `p-topics p-topics-index/show` | topic variants, editor shell, comments, quotes, spoilers, media | shared `main_code_*` | mapped |
| Critiques | `/forum/critiques` | `p-topics p-topics-index` | critique topics, ratings/votes, shortened text | shared `main_code_*` | mapped |
| Clubs | `/clubs`, `/clubs/90-klub-druzey` | `p-clubs p-clubs-index/show` | club cards/menu, users, comments, editor shell | shared `main_code_*` | mapped |
| Collections | `/collections`, `/collections/22806-nnhh` | `p-collections p-collections-index/show` | collection topics, catalog entries, votes, comments | shared `main_code_*` | mapped |
| Articles | `/articles`, `/articles/516-golubaya-shkatulka-idealnoe-anime-dlya-fanatov-shkolnoy-zhizni-i-romantiki` | `p-articles p-articles-index/show` | article topics, swiper/images, shortened text, comments | shared `main_code_*` | mapped |
| Users and profile | `/users`, public profile representative | `p-users p-users-index`; `p-profiles p-profiles-show` | user cards, profile summary, stats, friends/clubs/favourites, comments | shared and `prof_form_*` | mapped |
| Profile lists | `/:profile/list/anime`, `/:profile/list/manga`, `/:profile/list/visual_novel` | `p-user_rates p-user_rates-index p-profiles p-profiles-index` | list switchers, tables/lines, search, collection filters; VN empty state | shared and `prof_form_*` | mapped |
| Profile utilities | `/:profile/achievements`, `/:profile/publications`, `/:profile/custom_lists/anime`, `/:profile/edit/account` | `p-achievements-index`; `p-profiles-publications`; `p-custom_lists-index`; `p-profiles-edit` | achievements/badges, empty states, forms, OAuth token block | shared and `prof_form_*` | mapped |
| Profile messages | `/:profile/messages/news` | `p-messages p-messages-index p-profiles p-profiles-index` | message/news rows, embedded catalog entries and tooltips, unread markers | shared and `prof_form_*` | mapped |
| Calendar | `/ongoings` | `p-pages p-pages-ongoings` | catalog grid, options, comments/editor | shared `main_code_*` | mapped |
| About | `/about` | `p-pages p-pages-about` | lists, stats chart, comments/editor | shared `main_code_*` | mapped |
| Utility indexes | `/useful`, `/contests`, `/moderations` | `p-user_tools-index`; `p-contests-index`; `p-moderations-show` | sparse/empty page shells and moderation link lists | shared `main_code_*` | mapped |
| Global navigation/search | any mapped page | inherited page class | top menu, VN icons, random-page controls, opened global search modes/results/shade | shared `main_code_*` | mapped |
| Catalog filter states | `/animes` | `p-animes_collection p-animes_collection-index` | opened side menu; `genres_v2`; country mode toggle; season/range selectors; opened `year-dropdown` | shared `main_code_*` | mapped |

### Confirmed selector gaps

- VN navigation and entries: `icon-visual_novel`, `icon-visual_novel_list`, `c-visual_novel`, `b-platform-tag`, `b-genre-tag`.
- MAL score presentation: `scores`, `mal-based`, `collection_score_mal_icon`.
- Random-page controls: `random-anime-btn`, `random-anime-btn-mobile`, `random-anime-button`.
- Catalog controls: `season-selector*`, `range-selector*`, `year-dropdown*`, and `genres_v2`.
- Global search is substantially covered; only the newer `is-search-shade` state has no direct selector.

## shikimori.io

Populate after the `.rip` checkpoint by comparing equivalent templates.

| Area | Representative URL | Body page class | Differences from `.rip` | CSS scope | Status |
| --- | --- | --- | --- | --- | --- |

## Optional modules

| Module | Intended surface | Result | Status |
| --- | --- | --- | --- |
| `q01`–`q12` | See `engitheme/config/theme_files.json` | Pending `.rip` core coverage | mapped |

## Current checkpoint

- Local branch: `codex/shikimori-compatibility`.
- Remote fork setup is waiting for GitHub CLI re-authentication.
- Public and safe authenticated `.rip` templates above are mapped without storing account content.
- Detail-state follow-up remains for an individual dialog and any page-specific popup discovered during CSS work.
- No compatibility CSS changes have been made yet.
