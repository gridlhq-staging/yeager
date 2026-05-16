## Validation commands (run after edits)

You MUST run the relevant checks below after every code change, even for seemingly simple edits:

```bash
# Vet the package you changed
go vet ./path/to/package/...

# Run related tests (single package, single test)
go test ./path/to/package/... -run TestName -v -count=1

# Check formatting
gofmt -l path/to/file.go
```

## Go workflow rules
- After writing new .go files with new imports, run `go mod tidy` before `go test`

## Permissions
Allowed without asking: read files, go vet, gofmt, run single package tests
Ask first: go mod tidy, package installs, git push, deleting files, full test suite
