# Method — reproduce this on your own handle

All data is public (no login). Steps:

1. **Pull post history.** Use the public AT Protocol AppView `app.bsky.feed.getAuthorFeed` for your handle, paging through ~30 days.
2. **Separate roots from replies.** A post is a "root" if it is not a reply; link each reply to its root URI.
3. **Extract features per post:** timestamp (store UTC), text, whether it has an embed/link-card, likes/reposts/replies/quotes, and a topic label (keyword-bucket the text).
4. **Score:** `likes + 2·reposts + 1.5·replies + 2·quotes`.
5. **Aggregate:**
   - roots vs replies (mean score)
   - by topic (report sample size alongside the mean)
   - by hour-of-day and day-of-week (convert UTC → your local zone)
   - by opener type (does it start with a colored square? ALL-CAPS concept? prose?)
   - with vs without a link-card
6. **Find standouts:** replies whose score beats their own root — inspect them for shared structure.

### Honesty notes
- Report sample sizes; small-n topic results are advisory, not conclusions.
- Engagement is *measured*, never predicted.
- Don't over-generalize from one account — re-run on yours.
