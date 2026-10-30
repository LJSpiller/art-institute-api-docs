![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)
![Made with VS Code](https://img.shields.io/badge/Made%20with-VS%20Code-blue?logo=visual-studio-code)

# Art Institute of Chicago API: Documentation sample

An API documentation portfolio project. It documents three endpoints of the
public [Art Institute of Chicago API](https://api.artic.edu/docs) with an
OpenAPI 3.1 reference and interactive docs.

**Live docs:** https://LJSpiller.github.io/art-institute-api-docs/

## What this project demonstrates

- Authoring an OpenAPI 3.1 specification from observed API behavior
- Documenting a response envelope, pagination, and a consistent error format
- Scoping a large API (dozens of fields per artwork) down to the fields a new developer needs
- Publishing interactive reference docs with Scalar on GitHub Pages

## How the spec was built

The Art Institute publishes an OpenAPI file for its full API. For this sample, I wrote a focused spec covering three endpoints. I checked the endpoints, parameters, and error responses against live API calls, using the browser console and Swagger Editor's Try it out feature, and limited the spec to fields I saw in real responses. I could not render the complete published file in Swagger Editor.

## Endpoints covered

| Endpoint | Purpose |
| --- | --- |
| `GET /artworks` | List artworks with pagination |
| `GET /artworks/{id}` | Get one artwork |
| `GET /artworks/search` | Search artworks by keyword |

## Try it

No API key is required:

    curl "https://api.artic.edu/api/v1/artworks/search?q=monet&limit=2&fields=id,title,artist_title"

## Files

- `openapi.yaml`: the OpenAPI 3.1 specification
- `index.html`: renders the spec with Scalar

## Attribution

This is an unofficial sample and is not affiliated with the Art Institute of Chicago. Data is from the Art Institute of Chicago API. Per the API's license notice, the `description` field in the full API is licensed CC-BY 4.0 and all other data is CC0 1.0, subject to the museum's [Terms and Conditions](https://www.artic.edu/terms).

---

## License

This repo and its assets are licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://creativecommons.org/licenses/by-nc-nd/4.0/).

You may share this work with attribution for non-commercial purposes, but you may not remix or reuse it in derivative works.

This license covers the documentation and specification in this repo, not the Art Institute's data.