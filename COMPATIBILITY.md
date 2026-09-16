# Shikimori compatibility

Visual baseline: `Shikista` with `On Battle`. Secondary release palette: `Endless Horizon`.

Statuses: `mapped`, `patched`, `verified`, `limited`.

## shikimori.rip

| Area | Representative URL | Body page class | States/components | CSS scope | Status |
| --- | --- | --- | --- | --- | --- |
| Home | `/` | `p-dashboards p-dashboards-show` | catalog entries, news/topic previews, reviews, quotes, spoilers | shared `main_code_*` | mapped |
| Anime/manga/ranobe catalogs | `/animes`, `/mangas`, `/ranobe` | `p-animes_collection p-animes_collection-index` | pagination, catalog entries, collection filters, season/year/range selectors | `main_code_3.css` | verified |
| VN catalog | `/visual_novels` | `p-animes_collection p-animes_collection-index` | `c-visual_novel`, VN navigation/list icons, filters | shared `main_code_*` | verified |
| Anime/manga/ranobe entries | `/animes/52991-sousou-no-frieren`, `/mangas/4632-oyasumi-punpun`, `/ranobe/102875-fata-morgana-no-yakata-anata-no-genten-ni-itaru-monogatari` | `p-*-show p-db_entries p-db_entries-show p-animes p-animes-show` | poster actions, user rate, MAL/Shikimori scores, metadata, related entries, comments | `main_code_1.css`, `main_code_4mob.css` | verified |
| VN entry | `/visual_novels/37866-of-the-devil` | `p-visual_novels p-visual_novels-show p-db_entries p-db_entries-show p-animes p-animes-show` | platform/genre tags, VN rate, screenshots, empty comments | `main_code_1.css`, `main_code_2.css`, `main_code_4mob.css` | verified |
| Forum | `/forum`, `/forum/offtopic/5003548-spisok-izmeneniy` | `p-topics p-topics-index/show` | topic variants, editor shell, comments, quotes, spoilers, media | shared `main_code_*` | verified |
| Critiques | `/forum/critiques` | `p-topics p-topics-index` | critique topics, ratings/votes, shortened text | `main_code_2.css` | verified |
| Clubs | `/clubs`, `/clubs/90-klub-druzey` | `p-clubs p-clubs-index/show` | club cards/menu, users, comments, editor shell | shared `main_code_*` | verified |
| Collections | `/collections`, `/collections/22806-nnhh` | `p-collections p-collections-index/show` | collection topics, catalog entries, votes, comments | shared `main_code_*` | verified |
| Articles | `/articles`, `/articles/516-golubaya-shkatulka-idealnoe-anime-dlya-fanatov-shkolnoy-zhizni-i-romantiki` | `p-articles p-articles-index/show` | article topics, swiper/images, shortened text, comments | shared `main_code_*` | verified |
| Users and profile | `/users`, public profile representative | `p-users p-users-index`; `p-profiles p-profiles-show` | user cards, profile summary, stats, friends/clubs/favourites, comments | shared and `prof_form_*` | verified |
| Profile lists | `/:profile/list/anime`, `/:profile/list/manga`, `/:profile/list/visual_novel` | `p-user_rates p-user_rates-index p-profiles p-profiles-index` | list switchers, tables/lines, search, collection filters; VN empty state | shared and `prof_form_*` | verified |
| Profile utilities | `/:profile/history`, `/:profile/favorites`, `/:profile/achievements`, `/:profile/publications`, `/:profile/custom_lists/anime`, `/:profile/edit/account` | `p-user_histories-index`; `p-profiles-favorites`; `p-achievements-index`; `p-profiles-publications`; `p-custom_lists-index`; `p-profiles-edit` | history entry types, favourites, achievements/badges, empty states, forms, OAuth token block | shared and `prof_form_*` | verified |
| Profile messages | `/:profile/messages/news`, `/:profile/dialogs` | `p-messages p-messages-index`; `p-dialogs p-dialogs-index`; profile index classes | message/news rows, embedded catalog entries and tooltips, unread markers; empty dialog list | shared and `prof_form_*` | verified |
| Calendar | `/ongoings` | `p-pages p-pages-ongoings` | catalog grid, options, comments/editor | shared `main_code_*` | verified |
| About | `/about` | `p-pages p-pages-about` | lists, stats chart, comments/editor | shared `main_code_*` | verified |
| Utility indexes | `/useful`, `/contests`, `/moderations` | `p-user_tools-index`; `p-contests-index`; `p-moderations-show` | sparse/empty page shells and moderation link lists | shared `main_code_*` | verified |
| Global navigation/search | any mapped page | inherited page class | top menu, VN icons, random-page controls, opened global search modes/results/shade | `main_code_3.css` | verified |
| Catalog filter states | `/animes` | `p-animes_collection p-animes_collection-index` | opened side menu; `genres_v2`; country mode toggle; season/range selectors; opened `year-dropdown` | `main_code_3.css` | verified |

### Confirmed selector gaps

- VN tags and responsive entry types are patched. VN navigation and catalog cards already inherit established generic rules.
- MAL score presentation: `mal-based` patched; `scores` and `collection_score_mal_icon` already inherit sufficient parent rules.
- Random-page controls: `random-anime-btn` and `random-anime-btn-mobile` patched to inherit search colors; `random-anime-button` already inherits `b-link_button`.
- Catalog controls: `season-selector*`, `range-selector*`, `year-dropdown*`, and `genres_v2`.
- Critique score labels: `critique-stars .star-line .title` patched to use the existing white text variable.
- Global search is substantially covered; only the newer `is-search-shade` state has no direct selector.

## shikimori.io

Populate after the `.rip` checkpoint by comparing equivalent templates.

| Area | Representative URL | Body page class | Differences from `.rip` | CSS scope | Status |
| --- | --- | --- | --- | --- | --- |

## Optional modules

| Module | Intended surface | Result | Status |
| --- | --- | --- | --- |
| `q01` | Alternate user menu | Current profile entries ordered; VN icon/label covered; current text-fill cascade handled | verified |
| `q02` | Monocolor Citrus anime/manga lists | Citrus-only selectors match current anime/manga profile stats DOM | verified |
| `q03` | History entry-type markers | Current history links match; VN marker added with existing palette variables | verified |
| `q04` | Poster rating module in About Me | Deliberately reduced to an empty rule in project version 4.38; do not restore without evidence of current markup | limited |
| `q05` | Animated activity graph | Current profile has 60 lines; lines beyond the former 34 now inherit the established animation | verified |
| `q06` | Centered Over avatar | Over-only selectors match the current profile head DOM | verified |
| `q07` | Normal-width Over content with `q06` | Over-only profile, achievements and favourites selectors match current DOM | verified |
| `q08` | Alternate site menu | Current menu structure matches; VN database icon added to the existing group | verified |
| `q09` | Modified favourites | Current favourites structure matches; VN cards added by selector parity where no representative VN favourite is available | verified |
| `q10` | About Me component library | All three imported component files are present; custom About Me markup remains user-supplied | verified |
| `q11` | Squarer corners | Global selector already covers new controls and VN components; code-only check | verified |
| `q12` | Expandable Citrus Lite lists | Citrus Lite-only selectors match current anime/manga profile stats DOM | verified |

## Generator

| Area | Result | Status |
| --- | --- | --- |
| Theme asset loading | Uses the repository-relative `engitheme` directory locally and on GitHub Pages instead of the retired upstream site | verified |
| Profile formats | Shikista, Citrus, Citrus Lite and Over generate from their current sources | verified |
| BigShot | The only source is the original `.booody` placeholder from the initial commit; the format has deliberately remained hidden since commit `1685cfa` and no original profile CSS exists in repository history or GitHub code search | limited |

## Current checkpoint

- Local branch: `codex/shikimori-compatibility`.
- Fork: `DevLn737/ed-main.github.io`; `origin` points to the fork and `upstream` to `ed-main/ed-main.github.io`.
- The working branch is pushed and tracks `origin/codex/shikimori-compatibility`.
- Global navigation/search package verified in browser CSSOM with no size/layout change; the temporary verification style was removed.
- Catalog filters, MAL label and VN tags verified in browser CSSOM; temporary verification styles were removed. The responsive VN relation selector is retained by code analogy because the representative entry has no matching related VN card.
- Public social, profile, form/editor and utility templates were checked for visible stock light-theme colors. The only confirmed gap was the critique score label; its palette fix was verified in browser CSSOM and the temporary style was removed.
- `q01`, `q03`, `q05`, and `q08` changes were checked against current `.rip` desktop DOM/CSSOM; temporary rules and elements were removed. Format-specific modules were checked against their current target selectors without a full non-Shikista visual pass.
- `q04` remains the sole intentional limitation. The account has no representative VN favourite, so `q09` VN support is verified by the same current card structure rather than a populated live card.
- Public and safe authenticated `.rip` templates above are mapped without storing account content.
- An individual dialog is currently unavailable because the account dialog list is empty; page-specific popups remain follow-up during CSS work.
- Core `.rip` compatibility changes are present in `main_code_1.css`, `main_code_2.css`, `main_code_3.css`, and `main_code_4mob.css`.
- The generator now loads its checked-out `engitheme` assets. BigShot remains hidden because there is no original style to preserve or repair.
