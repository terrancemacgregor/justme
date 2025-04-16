# Blog Post Creation (FEAT-001)

## Description
Feature for creating and managing blog posts using MDX format with a WYSIWYG editor.

## Components
- WYSIWYG editor (TipTap)
- MDX processing
- Image upload to S3
- Preview functionality

## Technical Details
- Uses Contentlayer for type-safe content
- Integrates with S3 for media storage
- Supports frontmatter for metadata

## Related Commits
- `feat: add blog post editor [FEAT-001]`
- `improve: enhance image upload in editor [FEAT-001]`
- `fix: resolve MDX parsing issues [FEAT-001]`

## Dependencies
- TipTap
- Contentlayer
- AWS S3 SDK
- gray-matter 