# Solution Packaging

## Build Commands

```bash
dotnet build solution/File_Exporter_Component_Solution/File_Exporter_Component_Solution.cdsproj -c Release
```

Managed-only:

```bash
dotnet build solution/File_Exporter_Component_Solution/File_Exporter_Component_Solution.cdsproj -c Release /p:SolutionPackageType=Managed
```

## Output Location

- `solution/File_Exporter_Component_Solution/bin/Release/`

## Packaging Notes

- The Dataverse solution project references the PCF project directly
- The repo includes automatic version bumping during solution builds
- Managed and unmanaged solution packages are produced from the same build flow

## Minimum Release Checklist

- `npm run build` succeeds in the PCF project
- Solution build succeeds
- Import succeeds in the target environment
- Canvas app smoke test verifies:
  - `Disabled` mode
  - `Zip` mode
  - `Separate` mode
  - output JSON behavior
