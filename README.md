# ontarioislate.ca

Campaign site asking the Government of Ontario to proclaim the **Time Amendment Act, 2020**
(Bill 214), which ends the twice-yearly clock change and has never been brought into force.

Static site, no build step. `index.html` is self-contained; `og.png` is the link-preview
card and must sit beside it at the site root or social previews break.

## Cloudflare Pages settings

| Setting | Value |
|---|---|
| Framework preset | None |
| Build command | *(empty)* |
| Build output directory | `/` |

## Editing

Config constants sit at the top of the `<script>` block in `index.html`:

```js
const PREMIER = "premier@ontario.ca";
const AG      = "doug.downey@pc.ola.org";
const SITE    = "https://ontarioislate.ca";
```

Nothing is submitted anywhere. The letter is assembled in the visitor's browser and sent
from their own mail client. No backend, no analytics, no storage.

## The MPP roster

`MPPS` holds all 121 seated members of the 44th Parliament. **Every address was read from
that member's own page on ola.org.** None are pattern-guessed and none should be - the
domain varies by party and there are real irregularities:

- PC `@pc.ola.org`, but several are `...co@` (Ford, Kanapathi, Pang, Parsa, Surma, Tibollo, Anand)
- NDP `@ndp.on.ca`, mostly `-qp`, some `-co`; Tabuns is `tabunsp-` not `ptabuns-`
- Liberal `@liberal.ola.org` as `<initial><lastname>.mpp.co@` - except McCrimmon (`kmccrimmon-co@`) and Watt (plain `@ola.org`)
- Green and Independent: plain `@ola.org`
- Two Smiths in one party: David Smith is `david.smith1@pc.ola.org`
- **Guy Bourgouin (Mushkegowuk-James Bay) publishes no email.** The UI detects this and directs the writer to phone the office.

3 seats vacant: Hamilton East-Stoney Creek, Scarborough Southwest, York-Simcoe.
Re-verify the roster after any by-election.

## Facts that decay

- **Attorney General** - Doug Downey as of the 10 Sep 2026 shuffle. He holds the proclamation power, so if the portfolio moves, the site and the letters both change.
- **Alberta** - listed DONE on its commitment to year-round daylight time.
- **Quebec** - listed WAITING. If Quebec proclaims, the framing changes completely.
- **Sunshine Protection Act** - pending in the US Senate.

## Sourcing

Every figure is footnoted in the site footer. Keep it that way - the campaign's only asset
is that anyone who checks a claim finds it correct. The counterargument for permanent
*standard* time is stated fairly in the objections section and should stay there.

Independent volunteer campaign. No funding, no party affiliation.
