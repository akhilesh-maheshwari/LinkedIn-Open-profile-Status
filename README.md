# LinkedIn Open Profile Status Checker

Check whether a LinkedIn profile has **Open Profile** enabled, allowing people outside the member's network to send messages without using InMail credits.

Submit a single LinkedIn profile URL or a bulk list to retrieve Open Profile status (`true` or `false`), along with additional profile details. Built for lead qualification, outbound prospecting, and LinkedIn outreach workflows.

---

## Input Options

| Option | What You Provide |
|---|---|
| Single Profile | One LinkedIn profile URL |
| Bulk Profiles | Multiple LinkedIn profile URLs to check in one run |

---

## Data Fields Returned

| Field | Description |
|---|---|
| `Person` | Member's full name |
| `LinkedIn URL` | Member's LinkedIn profile URL |
| `Open Profile` | `true` if Open Profile is enabled; `false` if it is not |
| `Headline` | Member's LinkedIn profile headline |
| `Location` | Location listed on the member's profile |
| `Premium` | Indicates whether the member has LinkedIn Premium |
| `Influencer` | Indicates whether the member is marked as a LinkedIn influencer |
| `Distance` | Connection degree returned for the profile |
| `Followers` | Number of followers |
| `Connections` | Number of connections |

> **Note:** LinkedIn Premium and Open Profile are separate indicators. A Premium membership alone does not mean Open Profile is enabled.

---

## Sample Output

```json
{
  "Person": "Henry Williams",
  "LinkedIn URL": "https://www.linkedin.com/in/henry-williams-3071aabb",
  "Open Profile": true,
  "Headline": "Learning from 5 Founders Daily | Sharing What's Working in GTM & Sales | Still Figuring It Out",
  "Location": "Greater Edinburgh Area",
  "Premium": true,
  "Influencer": false,
  "Distance": "THIRD_DEGREE",
  "Followers": 3063,
  "Connections": 3031
}
```

---

## Use Cases

- **Qualify leads** — Identify prospects with Open Profile enabled before starting outreach.
- **Check existing lists** — Review Open Profile status across a bulk list of LinkedIn URLs.
- **Segment prospects** — Separate profiles by Open Profile status for different outreach workflows.
- **Enrich lead records** — Add headlines, locations, follower counts, and other returned profile details.

---

## How to Use

1. Create an [Apify](https://apify.com) account or sign in.
2. Open the **LinkedIn Open Profile Status Checker** actor.
3. Enter a single LinkedIn profile URL or a bulk list of URLs.
4. Run the actor.
5. Review the results and export your dataset.

---

## Understanding the Results

| Open Profile Status | Meaning |
|---|---|
| `true` | Open Profile is enabled. You can message this person from outside their network without using InMail credits. |
| `false` | Open Profile is not enabled. Other messaging options depend on your connection level and LinkedIn access. |

> Open Profile status reflects the member's settings at the time of the check and may change later.

---

## Notes

- No cookies or LinkedIn session required.
- Works for both single profile lookups and bulk runs.
- Results can be exported in JSON, CSV, or other formats supported by Apify.
