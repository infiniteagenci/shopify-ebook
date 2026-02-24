# Performance Optimization

I’ll never forget the day my store went from “fast enough” to “fast enough to convert.” After months of tweaking, I finally hit LCP under 2 seconds. That very afternoon, my mobile conversion rate jumped 22%. It wasn’t magic—it was deliberate, sometimes boring, work. But it’s some of the most impactful work you’ll ever do.

Performance isn’t just about scores; it’s about money. Every second of load time costs you trust and sales. Let’s fix that.

> **Founder’s Confession**  
> I installed 30 apps because “everyone said I needed them.” My site took 6 seconds to load. I deleted 20 and doubled my conversion. App bloat is real—and it’s killing your store.

## 1. Diagnosing Performance Problems

### Core Web Vitals (CWV) Benchmarks

Google uses these as ranking factors. Aim for:

- **LCP** (Largest Contentful Paint): < 2.5s
- **INP** (Interaction to Next Paint): < 200ms
- **CLS** (Cumulative Layout Shift): < 0.1

**How I test:** I run PageSpeed Insights on my homepage, top product, and checkout every week. It’s a habit.

### Common Performance Bottlenecks

From my own debugging:

1. **Huge images** – I once had a hero image at 2MB. It took 4 seconds to load. Compress to <150KB.
2. **App JavaScript** – Each app adds scripts. Ask: “Does this app directly make money?” If not, remove it.
3. **Render‑blocking CSS/JS** – Non‑critical stuff should load later.
4. **Web fonts** – Use system fonts or preload critical ones.
5. **Third‑party scripts** – Chat, heatmaps, analytics—load them only where needed.
6. **Theme code bloat** – Unused sections, heavy animations.

> **Take a Breath**  
> You don’t need a perfect score. Get into the “good” range (green on PageSpeed) and move on. Perfectionism stalls progress.

---

**Navigation**

- Next: [Marketing Attribution in a Privacy‑First World](marketing-attribution.md)

*End of Performance Optimization chapter*