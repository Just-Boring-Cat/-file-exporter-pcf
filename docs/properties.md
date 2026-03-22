# Properties And Outputs

## Inputs

- `documentsJson`: JSON array of document definitions
- `downloadMode`: `Disabled | Zip | Separate`
- `archiveFileName`: archive name for ZIP downloads
- `displayModeInput`: `Edit | Disabled | View`
- `buttonText`
- `fillContainer`
- `buttonType`: `Primary | Secondary | Outline | Text`
- `colorPalette`
- `fontFamily`
- `fontSize`
- `fontColor`
- `fontWeight`: `Normal | Semibold | Bold`
- `fontStyle`: `Normal | Italic`
- `textDecoration`: `None | Underline | Strikethrough`
- `textAlign`: `Left | Center | Right`
- `verticalAlign`: `Top | Middle | Bottom`
- `borderStyle`: `None | Solid`
- `borderWidth`
- `borderColor`
- `borderRadius`
- `paddingTop`
- `paddingRight`
- `paddingBottom`
- `paddingLeft`

Default padding values are `0`.

## Events

- `OnSelect`

## Outputs

### Main output payloads

- `documentsOutputJson`: processed per-document output JSON
- `downloadResultJson`: result of the last attempted built-in download action

### Status outputs

- `documentCount`
- `validDocumentCount`
- `isValid`
- `errorMessage`
- `lastAction`
- `changeToken`
- `selectToken`

## `documentsOutputJson` shape

Each document entry includes:

- `id`
- `fileName`
- `fileExtension`
- `fullFileName`
- `mimeType`
- `contentText`
- `base64`
- `sizeBytes`
- `isValid`
- `errorMessage`

## `downloadResultJson` shape

The last built-in download result includes:

- `mode`
- `action`
- `attemptedCount`
- `downloadedCount`
- `skippedCount`
- `fileNames`
- `errors`

## Notes

- `archiveFileName` is ignored unless `downloadMode = Zip`
- `Separate` mode is best-effort because multiple browser downloads can be restricted
- `Disabled` mode is the recommended path when a Flow or external system should handle storage
