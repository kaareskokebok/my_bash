# Files and directories

## zip and unzip

### Unzipping all zip-files and removing them after successful unzip
```bash
process_zip_files() {
  for zip in *.zip; do
    if unzip "$zip"; then
      echo "Successfully unzipped $zip"
      rm "$zip"
    else
      echo "Failed to unzip $zip"
    fi
  done
}

# Call the function
process_zip_files
```
