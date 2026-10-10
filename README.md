# RoktoSheba (রক্তসেবা)

Bengali-first, mobile-first website for RoktoSheba home blood sample collection enquiries in Gazipur, Bangladesh.

## Live site

After the GitHub Pages workflow completes:

- https://drkahridoy.github.io/Roktosheba/

## Local development

```bash
npm ci
npm run dev
```

## Production build

```bash
npm run build
```

The site is deployed through `.github/workflows/deploy-pages.yml` using GitHub Pages. The booking form is an enquiry fallback that opens a prefilled WhatsApp message; it does not create a persistent appointment record.
