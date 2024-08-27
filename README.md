/* @import url("https://raw.githubusercontent.com/Astatoru/Shikimori-Dark-Theme-Fork/master/shikimori_dark.css"); */

html,
body {
  color-scheme: dark;
  background: var(--bckg-primary);
}
:root {
  --bckg-primary: #212121;
  --bckg-dark: #1a1a1a;
  --bckg-light: #333333;
  --bckg-lighter: #454545;

  --txt-primary: #fff;
  --txt-secondary: #ccc;
  --txt-secondary-dark: #afafaf;
  --txt-accent: var(--clr-main-light);

  --clr-main-primary: var(--my-clr);
  --clr-main-dark: color-mix(in srgb, var(--clr-main-primary), black 30%);
  --clr-main-light: color-mix(in srgb, var(--clr-main-primary), white 15%);

  --link-primary: var(--clr-main-light);
  --link-hover: color-mix(in srgb, var(--link-primary) 60%, white);
  --link-active: color-mix(in srgb, var(--link-primary) 70%, white);

  --selection-bckg: #5292d280;
  --selection-search: #00ff0839;

  --def-icon: url("//shikimori.one/assets/layouts/l-top_menu-v2/glyph.svg");

  /* Активность на сайте бары */
  --bar-main: var(--my-clr);

  --my-clr: #5292d2;

  --xmas: initial;
  --halloween: initial;
  --icon: initial;
  --themes: initial;
  --dropdown: initial;
}

html[data-color-mode="light"] {
  --icon-color: var(--txt-secondary);
  --link-color: var(--link-primary);
  --link-hover-color: var(--link-hover);
  --link-active-color: var(--link-active);
  --headline-color: var(--my-clr);
  --headline-hover-color: var(--my-clr);
  --headline-background-color: var(--bckg-primary);
  --headline-border-color: var(--clr-main-primary);
}

/* #main */
.l-page {
  background-color: var(--bckg-light);
}

/* #select text*/
::selection {
  background: var(--selection-bckg) !important;
  color: currentColor !important;
}

/* #arrow to top слева полоска  */
.b-to-top.active .arrow {
  color: var(--txt-primary);
}
.b-to-top .slide:before {
  background-color: var(--bckg-lighter);
}

/* #global search */

.l-top_menu-v2 .global-search .search-results {
  &,
  .nothing_found,
  .search-mode {
    background: var(--bckg-dark);
    color: var(--txt-primary);
    border-color: var(--clr-main-dark);
  }
  /* remove shadow #search  */
  &::after,
  &::before {
    content: none;
  }
  /* #search left border */
  :is(
      .nothing_found.active,
      .nothing_found:focus,
      .b-db_entry-variant-list_item.active,
      .b-db_entry-variant-list_item:focus,
      .search-mode.active,
      .search-mode:focus
    ):before {
    background: var(--clr-main-primary);
  }
  /* border colored when active */
  .search-mode.active {
    background: none;
    border-top-color: var(--clr-main-light);
    & + .search-mode {
      border-top-color: var(--clr-main-light) !important;
    }
  }
  .search-mode:hover:before {
    background: var(--clr-main-dark);
  }
}
/* Set different #elements to text #secondary  */
.b-tag,
header.head .notice,
.b-stats_bar .title,
:is(.b-user_rate, .b-catalog_entry-tooltip) .inner :is(.rating .text, .rating),
.b-catalog_entry .cover .misc span,
.p-profiles-show .profile-content .activity .title,
.p-profiles-show .lifetime .times .time.checked,
.p-profiles-show .achievements .header .title,
.b-news_line-topic .status-line,
.p-profiles .profile-head .c-info .c-additionals b,
.p-user_rates-index .list-groups .summary.lines,
.bar.vertical .line .x_label,
.bar.horizontal .line .x_label,
.b-entry-info .line .value,
.b-rate .score-notice,
.b-animes-menu .total-rates,
.b-review-topic.is-review_review_author_details
  > .inner
  .review-details
  .b-status-line,
.b-review-topic.is-review_review_author_details
  > .inner
  .review-info
  .user-rate-label,
.b-comment > .inner .name-date .time,
.b-db_entry-variant-list_item > .info .line .key,
.profile-actions
  :is(
    .mail,
    .settings,
    .ban,
    .talk,
    .fav-add,
    .ignore-add,
    .fav-remove,
    .ignore-remove
  ),
.b-comment > .inner .name-date a.name .normal,
.b-catalog_entry-tooltip .inner .additional-images .link .title,
.l-top_menu-v2.is-search-focus .global-search .search-marker,
:is(.b-user.detailed,.b-user.b-user.moderation) .history .line .event,
.item-add,
.p-contests .rating .member .position, /* турнир: внизу список */
.p-contests .match-day .match-link.voted-none > .c-column a,
.p-contests .match-day .match-link.voted-left > .c-column:last-child a,
.p-contests .match-day .match-link.voted-right > .c-column:first-child a,
.p-contests .match-day .matches-num /* турнир: проценты*/,
.b-status-line :is(.section.main .comments,.section.created_at time):before,   /* Иконки в топиках(перо звезда) */
.b-status-line .section.main .collection-size,
.b-critique_votes:before,
.b-news_wall-topic .status-line .comments, /* НОвости коменти*/
.b-news_wall-topic .status-line .is-pinned:before, /* форум закреп */
.buttons .item-quote.is-active, /* Цитировать */
:is(.p-userlist_comparer-show,.p-recommendations-index,.p-mangas_collection-index,.p-animes_collection-index) .pagination,   /* Список тайтлов  */
.b-table th, /* Совместимость имя */
.b-header_filters .filter-line :is(a.current,.title), /* персонализированые */
.b-contest_match .current-match .match-members .vs *,  /* tournaments VS */
.tooltip-details .b-nothing_here.centered, /* коментарий был удален... */
.b-achievement :is(.about,.c-about)  .percent, /* /user/achievements текст */
.p-profiles-show .about .item-edit, /* profile edit about pencil */ 
.l-top_menu-v2 .submenu>a.icon-mail:hover span.unread span, /* сообщение в менюшки. цвет 0|2|0 */
.b-status-line .section.main .is-pinned:before,
.b-entry-info .line .key, /* achievements/common */
.b-options-floated.count, /* турнир: кандидаты справа */
.b-animes-menu .menu-topics-block .entry .time, /* Тайтл: Новости время */
.p-user_rates-index .list-lines tr :is(.name a,.index) /*Списки аниме\манги: название тайтла и номер */ {
  color: var(--txt-secondary);
}

.b-critique-topic .critique-stars .title,
.p-contests .match-day > .date :is(.from, .to) {
  color: var(--txt-primary);
}

.p-user_rates-index .list-lines tr td .episodes_total,
.b-subposter-action,
.l-top_menu-v2 .global-search .clear,
.l-top_menu-v2 .global-search,
.p-contests .match-day .match-link .c-column.loser a,
.p-contests .match-day .match-link .c-column.created a {
  color: var(--txt-secondary-dark);
}

.p-topics header h1 a.reload {
  color: var(--txt-accent);
}
/* Set different #elements to text primary  */

:is(.b-user_rate, .b-catalog_entry-tooltip) .inner .line .key,
.p-user_rates-index .l-content .order-control,
.b-block_list li,
.b-rate .text-score,
h2,
h3,
h4,
header.head h1,
header.head h2,
.b-news_wall-topic .title /* #main a>div */ {
  color: var(--link-primary);
}
/* bb-code */
/* textarea example */
.b-bb_codes-examples .example .textarea {
  background: var(--bckg-light);
  color: var(--txt-primary);
}

/* tabs colored */
[data-dynamic="tabs"] [class*="button"] {
  --tabs-button: var(--my-clr);
  background-color: var(--bckg-light);
  &:not(.active) {
    background-color: var(--bckg-light);
  }
  &:hover,
  &:not(.active):active {
    background-color: color-mix(in srgb, var(--tabs-button), #000 40%);
  }
  &.active {
    background-color: color-mix(in srgb, var(--tabs-button), #000 30%);
  }
}

/*border-left: spoiler,quote  */
.b-quote-v2,
.b-spoiler_block > div {
  border-color: var(--bckg-lighter);
}

/* end bb-code */

/* #tooltip (hover title) */
.tooltip-inner,
:is(.p-animes-franchise, .p-mangas-franchise, .p-ranobe-franchise)
  .sticky-tooltip {
  background-color: var(--bckg-light);
  color: var(--txt-primary);
  border-color: var(--bckg-light);
  box-shadow: 0 0 2px var(--txt-primary);
}
/* remove default #arrow on left side and set custom  */
.tooltip-arrow {
  visibility: hidden;

  &::before {
    content: "";
    display: block;
    visibility: visible;
    border: 24px solid #0000;
    border-right-color: var(--bckg-primary);
    position: absolute;
    left: -26px;
  }
  .tooltip-left &::before {
    left: 0;
    border-right-color: #0000;
    border-left-color: var(--bckg-primary);
  }
}
/* remove close #button */
:is(.sticky-tooltip, .tooltip-inner) .close {
  display: none;
}

/* #form action list and list title */
:is(.b-user_rate, .b-catalog_entry-tooltip)
  .b-add_to_list
  :is(.trigger, .option),
.b-add_to_list :is(.trigger, .option) {
  color: var(--link-color) !important;
  background: var(--bckg-primary) !important;
  border-color: var(--bckg-dark) !important;
}
:is(.b-user_rate, .b-catalog_entry-tooltip)
  .b-add_to_list
  :is(.trigger, .edit) {
  color: var(--clr-main-primary);
}
.b-add_to_list .trigger-arrow {
	  color: var(--link-color) !important;

  }
/* #profile */
.b-stats_bar .stat_names .stat_name a {
  color: var(--txt-secondary);
}

/* #hover faq */
.tipsy-inner {
  box-shadow: none;
  background-color: var(--bckg-dark);
}
.tipsy.tipsy-normal.tipsy-s {
  opacity: 1 !important;
}

/* #hover #tournaments  */
.p-contests .match-day .match-link.active {
  background-color: var(--bckg-light);
}
.p-contests .match-day .match-link:hover {
  background-color: var(--bckg-dark);
}
/* style #bars for profile  */
/* список аниме на профиль цвета */
.b-stats_bar {
  /* текст изменить */
  --link-color: color-mix(in srgb, var(--first), #fff 60%);
  --link-hover-color: color-mix(in srgb, var(--first), #fff 70%);
  &.anime {
    --first: #79a9cf;
  }
  &.manga {
    --first: #cc69ad;
  }
  &.lifetime {
    --first: var(--bar-main);
  }
  .stat_names .stat_name a {
    color: var(--link-color);
  }
}

.b-stats_bar:is(.anime, .manga, .lifetime) .bar {
  .first {
    background-color: var(--first);
  }
  .second {
    background-color: color-mix(in srgb, var(--first), #000 20%);
  }
  .third {
    background-color: color-mix(in srgb, var(--first), #000 40%);
  }
  :is(.first, .second, .third):hover {
    background-color: color-mix(in srgb, var(--first), #000 20%);
  }
}
/* Профиль: Активность на сайте */
.bar.simple .bar {
  &.s0 {
    --bar-clr: color-mix(in srgb, var(--bar-main), #000 20%);
  }
  &.s1 {
    --bar-clr: color-mix(in srgb, var(--bar-main), #000 10%);
  }
  &.s2 {
    --bar-clr: color-mix(in srgb, var(--bar-main), #fff 5%);
  }
  &.s3 {
    --bar-clr: color-mix(in srgb, var(--bar-main), #fff 20%);
  }
  &:is(.s0, .s1, .s2, .s3) {
    background: var(--bar-clr);
    &:hover {
      background: color-mix(in srgb, var(--bar-clr), #000 10%);
    }
  }
}

/* #input style #button */
input,
select,
textarea,
.subheadline-input[type="submit"],
.subheadline-input[type="text"],
.subheadline-input[type="password"],
.subheadline-input[type="email"],
.b-form input,
.b-button,
.b-input input,
.b-form input[type="submit"],
.l-top_menu-v2 .global-search input,
.b-link_button.dark,
.b-form textarea,
.b-input textarea,
.b-shiki_editor .links .link-value,
.b-shiki_editor .images .link-value,
.b-shiki_editor .quotes .link-value,
.b-shiki_editor .upload .link-value,
.b-link_button,
.b-poll .poll-actions .vote,
.b-poll .poll-actions .abstain,
.b-collection_search .field input {
  background: var(--bckg-dark);
  color: var(--txt-primary);
  border: 1px solid var(--bckg-lighter);
}
.l-top_menu-v2 .global-search input {
  -webkit-border-radius:0px;
  border-radius:0px;
}
input:focus {
  border-color: var(--selection-bckg) !important;
}
.b-form input[type="submit"]:hover,
.b-button:hover,
.b-link_button.dark:hover,
.b-link_button:hover,
.b-poll .poll-actions .vote:hover,
.b-poll .poll-actions .abstain:hover {
  border-color: var(--selection-bckg);
  background-color: var(--selection-bckg);
}
.b-form.green-form {
  background: var(--bckg-dark);
  border-color: grey;
}
.b-input input[disabled] {
  background-color: var(--bckg-light);
}
.l-top_menu-v2 .global-search input {
  background-color: rgba(0, 0, 0, 0.3);
  border-color: rgba(0, 0, 0, 0.3);
}
/* #input data  */
.pika-single,
.pika-label {
  color: var(--txt-primary);
  background: var(--bckg-light);
}
.pika-button,
.is-today .pika-button {
  background-color: var(--bckg-lighter);
  color: var(--txt-secondary) !important;
}
.pika-button:hover {
  background-color: var(--clr-main-dark);
}
.is-selected .pika-button {
  background-color: var(--clr-main-primary);
  box-shadow: none;
}
:is(.is-disabled, .pika-day) .pika-button {
  background-color: var(--bckg-dark);
}

/*   #message  */
.yellow-fade {
  outline: 10px solid var(--bckg-dark);
  background: var(--bckg-dark);
}
/* style for #list  */
.p-user_rates-index .list-lines tr td .rewatches {
  color: skyblue;
}
/* Списки: тайтл ховер */
.p-user_rates-index .list-lines .selectable:hover {
  background-color: var(--bckg-primary);
}
/*Списки: Изменение тайтла */
.p-user_rates-index .list-lines tr.edit-form form {
  background-color: var(--bckg-primary);
  border-top:none;
  border-bottom:none;
  margin:0px;
}
/* Списки: свернуто кнопка */
.collapsed {
  background-color: var(--bckg-primary);
  color: var(--txt-secondary);
  border: 0;
  &:hover {
    background-color: var(--bckg-lighter);
    color: var(--txt-secondary);
  }
}

/* Списки: справа чекбоксы */
.b-block_list li {
  height: 24px;
  margin: 0;
  display: flex;
  align-items: center;
  padding: 4px;
  &:hover,
  &.selected {
    background-color: var(--bckg-primary);
    color: var(--txt-primary);
  }
}

/* Списки: справа в хедлайне чекмарк */
.b-collection-filters .block > .filter {
  margin: 0;
  height: 30px;
  line-height: 30px;
}
/* #check radio #input  */
.b-radio input[type="radio"]:checked + .radio-label:before {
  border-color: var(--txt-accent);
}
/* #list plus/minus  */
.item-add:first-child {
  right: 0;
  display: grid;
  place-content: center;
}
/* #checkbox */
input[type="checkbox"] {
  accent-color: var(--clr-main-dark);
}

/* mini #checkbox */
.p-contests .match-day .match-link.voted-abstain .started:before {
  color: var(--clr-main-dark);
}
/* #avatar style  */
.avatar img[alt],
.icon-avatar img,
.profile a img[alt],
.image-name .image {
  border-radius: 50% !important;
}

/* #main my-list dashboard  */
.p-dashboards-show .v2 .my-list {
  background: var(--bckg-primary);
  border: 0;
  .label span {
    color: var(--txt-primary);
  }
  .b-user_rate-history :is(.status-counter, .score-time time) {
    color: var(--txt-secondary);
  }
}
/* old style main page dashboard*/
.p-dashboards-show .cc-second .cc-inner .c-my_list {
  background: var(--bckg-primary);
  border-color: var(--txt-secondary);
}

/* аниме манга ранобе на главной */
.p-dashboards-show .v2 .fc-user-sections .f-sections {
  display: grid;
  & :is(.f-headline, .f-tags) {
    width: 100%;
  }
  .fc-tags {
    position: relative;
    display: flex;
  }
  .tag-link {
    background-color: var(--tag-color);
    border: 0;
    &.anime-tag {
      --tag-color: darkred;
      color: lightcoral;
    }
    &.manga-tag {
      --tag-color: darkblue;
      color: dodgerblue;
    }
    &.ranobe-tag {
      --tag-color: darkgreen;
      color: springgreen;
    }
    &:hover {
      background: color-mix(in srgb, var(--tag-color), #000 20%);
    }
  }
}

/* #headline  */
.headline,
.midheadline,
.linkheadline,
.subheadline {
  --hl-clr: currentColor;
  background: var(--headline-background-color);
  border-color: currentColor;
  & > a:hover:before,
  & > a:hover {
    color: currentColor !important;
  }
}

/* /about графики */
.p-pages-about .traffic-chart,
.p-pages-about .comments-chart,
.p-pages-about .users-chart {
  rect{
    fill: var(--bckg-dark);
  }
  text {
    fill: var(--txt-secondary) !important;
  }
  /* попап при ховере */
  .highcharts-label-box{
    fill:var(--bckg-light)
  }
}

/* #offtop  */
.b-offtopic_marker.active:before,
.b-offtopic_marker.off:before,
.b-offtopic_marker.active:hover:before,
body[data-locale=ru] .b-offtopic_marker:before {
  background-color: #5c2940 !important;
  border: 2px solid #5c2940 !important;
}

/* new marker */
body[data-locale=ru] .b-new_marker:before {
  background-color:#537ca6 !important;
  border:none;
}

/* #main status tag */
.b-anime_status_tag {
  background-color: var(--bckg-primary);
  border: 0 !important;
  padding: 1px 6px !important;

  &.critique {
    background-color: PaleVioletRed;
  }
  &.contest {
    background-color: darkorchid;
  }
  &.news {
    background-color: sienna;
  }
  &.collection {
    background-color: darkgreen;
  }
  &.article {
    background-color: chocolate;
  }
  &.censored {
    background-color: MediumVioletRed;
  }
  &:is(.other, .) {
    background-color: var(--bckg-primary);
    color: var(--txt-primary);
  }
}

/* #status minified (#tournaments) */
.b-catalog_entry:is(
    .on_hold,
    .planned,
    .dropped,
    .watching,
    .rewatching,
    .completed
  )
  .user_rates-minified
  .image-decor:after {
  top: 0;
  right: 0;
  left: auto;
}
/* Ачивмент и Главная-Мой список: прогресс бар  */
:is(.b-achievement :is(.c-about, .about), .b-user_rate-history) .progress {
  background-color: var(--bckg-lighter);
  div {
    background: var(--clr-main-light) !important;
  }
}
/* #achievement сверху справа уведомление */
.b-achievements_notifier .achievement:is(.gained, .lost) {
  background: var(--bckg-dark);
}

/* #catalog #title status */
.b-catalog_entry:is(
    .on_hold,
    .planned,
    .dropped,
    .watching,
    .rewatching,
    .completed
  )
  .image-decor {
  &:before {
    display: none;
    top: 0;
    right: 0;
  }
  &:after {
    background-color: var(--bckg-primary);
    border: 2px solid currentColor;
    border-color: 0;
    top: 0;
    right: 0;
    border-radius: 0 0 0 8px;
  }
  .on_hold &:after {
    color: grey;
  }
  .planned &:after {
    color: lightgrey;
  }
  .dropped &:after {
    color: lightcoral;
  }
  .watching &:after {
    color: skyblue;
  }
  .rewatching &:after {
    color: #71c5f9;
  }
  .completed &:after {
    color: rgb(60, 204, 137);
  }
}

/* #title three dots and #comments loader   */
:is(.p-animes-show, .p-mangas-show, .p-ranobe-show) .other-names,
.b-comments :is(.comments-loader, .comments-hider, .comments-expander),
:is(.b-comments, .b-forum) .faye-loader {
  background-color: var(--bckg-dark);
  border-color: none;
  color: var(--txt-secondary);
  border: 1px solid var(--bckg-lighter);
}
:is(.p-animes-show, .p-mangas-show, .p-ranobe-show) .other-names:hover,
:is(.b-comments, .b-forum)
  :is(
    .comments-loader,
    .faye-loader,
    .comments-hider,
    .comments-expander
  ):hover {
  background-color: var(--selection-bckg);
  border-color: var(--selection-bckg);
  color: var(--txt-secondary);
}

/* #comments navigation  (Все отзывы,...)*/
.b-reviews_navigation .navigation-node {
  background-color: var(--bckg-primary) !important;
  color: var(--txt-primary);
  border-color: currentColor;
  &[class*="all"] {
    color: var(--txt-primary) !important;
  }
}
/* color to navigation and review rate */
:is(
    .b-reviews_navigation .navigation-node,
    .b-review-topic.is-review_review_author_details
      > .inner
      :is(.label, .opinion)
  ) {
  &[class*="neutral"] {
    color: skyblue;
  }
  &[class*="positive"] {
    color: LimeGreen;
  }
  &[class*="negative"] {
    color: crimson;
  }
}
/* empty reviews */
.b-reviews_navigation
  .navigation-node.is-empty:not(.is-active)
  :is(.label, .count) {
  color: currentColor;
  opacity: 0.4;
}

/* #comments rate review  */
.b-review-topic.is-review_review_author_details
  > .inner
  .review-info
  .opinion:is(.negative, .neutral, .positive) {
  background-color: #0000;
}
/* #forum comments style  */
.b-comment {
  border: 0;
  border-bottom: 1px solid var(--bckg-lighter);
  margin: 12px 0;
  padding: 8px 0;
}

/* #comments replies  */
.b-replies {
  position: absolute;
  right: 0;
  bottom: 0px;
}
/* #title comments style  */
.b-topic {
  border: 0;
  border-bottom: 1px solid var(--bckg-lighter);
  margin: 16px 0;
  padding-top: 4px;
}
/* #spoiler block  */
.b-spoiler_inline:not(.is-opened) {
  background-color: var(--bckg-dark);
}

/* #comments shade off  */
.body.b-text_with_paragraphs {
  position: relative;
}
.b-height_shortener .shade {
  filter: invert(0.7);
}

/* #comments buttons  */
.main-controls
  :is(
    .item-moderation,
    .item-quote,
    .item-reply,
    .item-edit,
    .item-delete,
    .item-cancel,
    .item-ignore
  ) {
  color: var(--txt-secondary-dark);
}

/* #comments editor  */

/* #image  */
.ProseMirror
  :is(
    [data-image],
    [data-div],
    [data-link],
    [data-span],
    [data-video],

  ):hover:before {
  background-color: var(--bckg-lighter);
  color: var(--txt-accent);
  box-shadow: none;
  text-shadow: none;
}

.vue-node .menubar {
  background-color: var(--bckg-dark);
}
.vue-node .unsaved-content {
  background: var(--bckg-lighter);
}
.vue-node .icons :is(button, label).icon,
.buttons .b-tooltipped {
  color: var(--txt-secondary);
}
.ProseMirror,
code.b-code_inline,
.b-shiki_editor .body .editor textarea:not([rows]) {
  background-color: var(--bckg-primary);
  border-color: grey;
  color: var(--txt-primary);
}
.b-spoiler_inline.is-opened {
  background-color: var(--bckg-dark);
}
code.b-code_inline {
  color: #ba3453;
}
.b-shiki_editor .controls {
  margin: 0;
  padding: 14px 4px;
  background-color: var(--bckg-dark);
}
.popup-content {
  background-color: var(--bckg-light) !important;
}
.b-quote-v2,
.b-spoiler_block > div,
.b-quote .quoteable:before {
  background-color: var(--bckg-dark);
  color: var(--txt-primary);
  border-color: var(--selection-bckg)
}
.b-spoiler_inline.is-opened:hover {
  background-color: var(--selection-bckg);
  cursor: pointer;
}
.b-spoiler_inline:not(.is-opened):hover  {
  background-color: var(--selection-bckg);
}
/* Text editor заголовок */
.b-spoiler_block
  > span
  > i:is(.edit, .expand, .center, .remove, .drag-handle):hover {
  background: var(--bckg-light);
}

.b-quote {
  background-color: var(--bckg-dark);
  color: var(--txt-primary);
  border: 2px solid grey;
}

/* feedback remove  */
.b-feedback {
  display: none;
}

/* #spoiler block  */
.b-spoiler .content .before,
.b-spoiler .content .after {
  color: var(--txt-accent);
}
/* b-ajax style  */

/* remove prev loader */

.b-ajax::before,
.b-ajax::after,
.ajax-loading,
.ajax-loading.vk-like {
  background: none;
}

.b-ajax::after,
.ajax-loading::before {
  display: grid;
  place-content: center;
  height: 24px;
  width: 24px;
}
.b-ajax::after,
.ajax-loading::before {
  content: "";
  inset: 0;
  position: absolute;
  margin: auto;

  border: 5px solid var(--txt-primary);
  border-bottom-color: #0000;
  border-radius: 50%;
  display: inline-block;
  box-sizing: border-box;
  animation: rotation 1s linear infinite;
}
@keyframes rotation {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/* #top #main menu  */
.l-top_menu-v2,
.x1000 .l-top_menu-v2 {
  background: var(--dropdown, var(--bckg-dark));
  position: sticky;
  inset: 0;
  margin: auto;
  max-width: 1200px;
}
/* новые уведомление: справа сверху квадратик */

.b-comments-notifier {
  background-color: color-mix(
    in srgb,
    var(--dropdown, var(--my-clr)),
    #000 40%
  );
  &:hover,
  &:active {
    background-color: color-mix(
      in srgb,
      var(--dropdown, var(--my-clr)),
      #000 30%
    );
  }
}
/* коменты и тд: значок "новое" */
.b-new_marker:before {
  color: var(--txt-sec) !important;
  background: var(--dropdown, var(--my-clr)) !important;
  border: 0 !important;
  padding: 2px;
}
/* dropdown menu background*/
.l-top_menu-v2 .menu-dropdown > span[tabindex] {
  background: color-mix(in srgb, var(--dropdown, var(--bckg-dark)) 80%, white);
}
.l-top_menu-v2 .menu-icon:is(:active, :focus),
.l-top_menu-v2 .menu-dropdown.active > span[tabindex],
.l-top_menu-v2 .menu-icon:hover,
.l-top_menu-v2 .menu-dropdown.active > span[tabindex]:hover,
.l-top_menu-v2 .menu-dropdown > span a:is(:hover, :active, :focus) {
  background: color-mix(in srgb, var(--dropdown, var(--bckg-dark)) 70%, white);
}

.l-top_menu-v2 .submenu > a {
  background-color: var(--bckg-primary);
}
.l-top_menu-v2 .submenu > a:is(:hover, :active) {
  background-color: var(--bckg-lighter);
  color: var(--txt-primary);
}
.l-top_menu-v2 .submenu > .legend {
  background: var(--bckg-light);
  color: var(--txt-secondary);
  text-align: center;
  margin: 0 !important;
  padding: 2px 0;
}

/* #forum header  */
header.head {
  border-bottom: 2px solid var(--bckg-primary);
}
header.head h1 a.back:before,
header.head h2 a.back:before {
  color: var(--txt-secondary);
}
/* #footer */
.b-footer_vote {
  background: var(--bckg-dark);
  color: var(--txt-secondary);
  border-color: var(--bckg-lighter);
}

/* #topic hot-topic  */
.b-hot_topics-v2 {
  background: var(--bckg-primary);
}
.b-hot_topics-v2 .subject {
  color: var(--txt-secondary);
}

.b-input[data-v-3d684595] .ti-new-tag-input-wrapper .ti-new-tag-input,
.b-input[data-v-3d684595] .ti-input,
.vue-tags-input[data-v-13abcd46],
.ti-autocomplete[data-v-13abcd46] {
  background: var(--bckg-light);
  color: var(--txt-secondary);
}
/* editor is-loading */
.editor-container.is-loading[data-v-082d85bb]:before {
  background-color: #666a;
}

/* profile css editor  */
.b-edit_styles .edit_style .style_css .CodeMirror,
.b-edit_styles .new_style .style_css .CodeMirror,
.cm-s-solarized.cm-s-light {
  background-color: var(--bckg-primary);
  text-shadow: none;
  border-color: var(--bckg-light);
  border-right: none;
}
.CodeMirror-gutter,
.cm-s-solarized.cm-s-light .CodeMirror-linenumber {
  color: var(--txt-primary);
  background-color: var(--bckg-dark);
}
.cm-s-solarized.cm-s-light div.CodeMirror-selected {
  background: var(--selection-bckg);
}
.cm-searching {
  background-color: var(--selection-search);
}

/* #mobile toggler  */
.l-page .menu-toggler {
  width: 40px;
  height: 80px;
  position: fixed;
  top: calc(var(--top-menu-height) * 1.25);
}
.l-page .menu-toggler .toggler {
  position: absolute;
  display: grid;
  padding: 6px 8px;
  align-content: center;
  justify-items: center;
}
.l-page .menu-toggler .toggler,
.l-page .menu-toggler .toggler::after {
  background-color: var(--bckg-light);
  color: var(--txt-primary);
}
.l-page .menu-toggler .toggler::before {
  transform: none;
  writing-mode: vertical-lr;
  margin: 0;
}
/* Мой список на главной */
.p-dashboards-show .v2 .fc-user-sections .f-user {
  max-width: 320px;
  width: auto;
  /* для мобилки на всю длинну */
  @media screen and (max-width: 1023px) {
    max-width: none;
  }
}
.p-user_rates-index .list-groups .summary.posters,
.p-user_rates-index .list-groups .summary.lines.list {
  background: #0000;
  border: 0;
}
.p-user_rates-index .list-lines.b-table,
.list-posters.cc-5 {
  border-bottom: 1px solid grey;
}

.b-modal > .inner {
  background: var(--bckg-light);
}

.b-show_more,
.b-show_more-more .hide-more {
  color: #cecece;
}

/* /comparer/(anime|manga|ranobe)/[user]/vs/[user2] */
.p-userlist_comparer {
  /* general colors */
  & :is(.comparer table, .legend) .selectable,
  header.head .notice:first-of-type > span {
    --b-c: var(--bckg-light);
    background-color: var(--b-c) !important;
  }
  .comparer table .selectable:hover {
    background-color: color-mix(in srgb, var(--b-c), black 10%) !important;
  }
  /* list 'a' names */
  .comparer table .name a {
    color: #ccc;
  }
  /* adding colors to diff */
  & :is(.comparer table, .legend) {
    .almost-same {
      --b-c: #006400da;
    }
    .abslt-difr {
      --b-c: #b22222da;
    }
    .exact-same {
      --b-c: #2e8b57da;
    }
    .slightly-difr {
      --b-c: #f08080da;
    }
  }
  header.head .notice > span {
    &:nth-of-type(1) {
      --b-c: #006400da;
    }
    &:nth-of-type(2) {
      --b-c: #b22222da;
    }
    &:nth-of-type(3) {
      --b-c: #2e8b57da;
    }
    &:nth-of-type(4) {
      --b-c: #f08080da;
    }
  }
}

@media screen and (max-width: 1023px) {
  /* мобилка: стрелки на главной */
  .p-dashboards-show .v2 :is(.mobile-slider-prev, .mobile-slider-next) {
    width: 48px;
    top: 0;
    height: 100%;
    &::before {
      content: none;
    }
    &::after {
      width: 24px;
      height: 24px;
      background-color: color-mix(in srgb, var(--bckg-light), #0000 40%);
      border-radius: 50%;
      color: #fff;
      margin: 0;
      text-align: center;
      line-height: 24px;
      position: absolute;
      top: 50%;
      font-size: 12px;
      translate: 0 -50%;
      border: 2px solid #fff;
    }
    &:focus:after,
    &:active:after {
      color: #ccc;
    }
    /* для онгоингов */
    .fc-ongoings &:after {
      translate: 0 -100%;
    }
  }
  /* Главная: Мой список */
  .p-dashboards-show .v2 .fc-user-sections .f-user {
    max-width: none;
  }
}

/* news  */
.edit-page.styles .cc-2::before {
  content: "Shikimori-theme: создайте в :root --my-clr как основной цвет. Например: --my-clr: #00ff00\a  Добавляйте в :root строчки, чтобы:\a--news: none - отключить это окно:\a--dropdown: var(--my-clr) - верхнее меню изменить на основной цвет\a--link-primary: var(--my-clr) - сделать основной текст основным цветом (или каким хотите)\a--icon: var(--def-icon); - установить дефолт лого \a--themes: var(--my-clr) - отключить все темы (xmas, halloween и т.д.)\a--xmas: var(--my-clr) - отключить тему рождества\a--halloween: var(--my-clr) - отключить тему хэллоуин";
  white-space: pre-wrap;
  display: var(--news, block);
  font-size: 12px;
  float: left;
  position: relative;
  color: #cecece;
  background: var(--bckg-primary);
  z-index: 2;
  padding: 8px;
  margin-bottom: 10px;
}

/* themes */

/* halloween */
html:has(body:is([data-server_time*="11-01T"], [data-server_time*="10-31T"])) {
  --my-clr: var(--themes, var(--halloween, darkorange));
  --dropdown: var(--my-clr);
  & .l-top_menu-v2 .logo-container .glyph {
    background-image: var(--icon,url(https://raw.githubusercontent.com/Dedonych/Shikimori-Dark-Theme/master/icons/pumpkin.png));
  }
}

/* x-mas */
html:has(
    body:is(
        [data-server_time*="-12-2"],
        [data-server_time*="-12-3"],
        [data-server_time*="-01-01"],
        [data-server_time*="-01-02"],
        [data-server_time*="-01-03"],
        [data-server_time*="-01-04"],
        [data-server_time*="-01-05"]
      )
  ) {
  --my-clr: var(--themes, var(--xmas, #ba0000));
  --dropdown: var(--my-clr);
  & .l-top_menu-v2 .logo-container .glyph {
    background-image: var(--icon,url(https://raw.githubusercontent.com/Dedonych/Shikimori-Dark-Theme/master/icons/gift.png));
  }
}
/* Hide clubs and friends */
.m30.cc-2a {
	display: none;
}
/* Hide achievements */
.achievements.block {
	display:none;
}
/* Hide about me headline */
.block.about > .subheadline {
	display: none;
}
/* Hide links at the bottom */
.l-footer {
	display: none;
}
/* Hide arrow */
.active.b-to-top {
	display: none;
}
/* Hide third item in the history list */
div.entry:nth-of-type(3) {
	display: none;
}
/* Hide reviews */
.b-reviews_navigation {
	display: none;
}
/* Hide links under information tab */
.additional-links > .line-container {
	display: none;
}
/* Hide description source */
.description-current > .b-source {
	display: none;
}
/* Reorder blocks in profile */
.bubbled-processed {
	text-decoration: initial;
}
.c-column.c-left {
	display: none;
}
.c-column.c-right.c-right.c-right {
	width: 100%;
}
.b-user.c-column.avatar {
	width: auto;
	margin-right: 1%;
	float: none;
}
.b-club.c-colum.avatar {
	width: auto;
	margin-right: 0;
}
/* Sticky header */
@media screen and (min-width: 1025px) {
.l-top_menu-v2 { position: sticky; top: 0;
		}
.l-top_menu-v2 .active .submenu {
max-height: calc(100vh - var(--top-menu-height)); overflow-y: auto;
	}
}
/* Add some pixels at about me block bottom */
.block.about {
    border-bottom-width: 30px;
    border-bottom-style: solid;
    border-bottom-color: #333333;
    margin-bottom: 0px;
}
/* Add some pixels at comments block bottom */
.shiki_editor-selector.b-shiki_editor-v2 > footer {
    border-bottom-width: 30px;
    border-bottom-style: solid;
    border-bottom-color: #333333;
    margin-bottom: 0px;
}
/* Studio tag color */
.studio.b-anime_status_tag {
    background-color: var(--selection-bckg);
    border: 1px solid var(--bckg-lighter) !important;
    color: var(--txt-primary);
}
.b-anime_status_tag.studio[href]:hover {
    background-color: var(--my-clr);
}
/* User list anime status */
.p-user_rates-index .list-lines tr td .anons {
  color:#f34b4b;
}
.p-user_rates-index .list-lines tr td .ongoing {
  color:#a9dc4f;
}
.p-user_rates-index .list-lines tr td .rate-text {
  color:#c497da;
}
