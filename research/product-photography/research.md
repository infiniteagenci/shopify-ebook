# Research Notes: Product Photography & Visual Content for Shopify

## Why It Matters
- Visuals are the primary driver of conversion in e-commerce
- High-quality images increase perceived value and trust
- Mobile shopping (70%+ traffic) demands crisp, fast-loading images
- Social media sharing relies on compelling visuals

## Key Requirements

### 1. Image Quality Standards
- Resolution: Minimum 2000x2000px (Shopify recommends 800x800 minimum)
- Format: JPEG for photos, PNG for graphics with transparency
- Compression: 70-80% quality, file size < 150KB per image (WebP preferred)
- Color space: sRGB for web consistency
- Background: Clean white or lifestyle context (consistent across catalog)

### 2. Image Types Needed
- **Hero/Featured Image**: High-resolution main product image
- **Gallery Images**: Multiple angles (front, back, side, detail shots)
- **Lifestyle Images**: Product in use, real-world context
- **Video**: 15-30 second product videos (auto-play on hover optional)
- **360° Views**: For high-value items (optional)

### 3. Technical Implementation on Shopify
- Use Shopify's CDN (auto-optimizes and serves WebP)
- Implement responsive images via `srcset` and `sizes` attributes
- Lazy load below-the-fold images (`loading="lazy"`)
- Set explicit width/height to prevent CLS
- Use `{{ img_url }}` filter with size parameters (e.g., `product.featured_image | img_url: '800x800'`)

### 4. Best Practices
- Consistent lighting and angles across product line
- Use a lightbox for zoom functionality (apps like Magic Zoom Plus)
- Allow thumbnail gallery on product pages
- Optimize for mobile: touch-friendly gallery, swipe support
- Include alt text for accessibility and SEO

### 5. Tools & Apps
- **Crush.pics** – Automatic image compression on upload
- **Magic Zoom Plus** – Magnifier zoom on product images
- **Vizard** or **Remove.bg** – Background removal
- **Cloudinary** – Advanced image transformations (if heavy catalog)

### 6. Common Mistakes
- Overly large images slowing down page speed
- Inconsistent style (different backgrounds, lighting)
- Too few images (less than 3 per product)
- No lifestyle shots (only white backgrounds)
- Ignoring mobile image quality

### 7. Emerging Trends
- User-generated content (UGC) galleries
- AR/3D product views (Shopify supports USDZ files)
- Video autoplay on product pages
- AI-generated lifestyle backgrounds

## Statistics
- 67% of consumers say good images are "very important" (Nielsen)
- Products with videos have 144% higher conversion (Animoto)
- 360° views can increase conversion by 27% (3D挚)
