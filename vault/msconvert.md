---
id: mrslbnp9bp5tia1ne4nnszu
title: Msconvert
desc: ''
updated: 1717318043406
created: 1717315977177
---

Setting up msconvert bot on commons-server

https://hub.docker.com/r/chambm/pwiz-skyline-i-agree-to-the-vendor-licenses

docker run -it --rm -e WINEDEBUG=-all -v /your/data:/data chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine msconvert /data/file.raw

docker run -it --rm -e WINEDEBUG=-all -v /media/share/mapp/public/QE_plus_unifr/raw/:/data chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine msconvert /data/1684941280_PMA_dbgi_000993_01_01_neg.raw

docker run -it --rm -e WINEDEBUG=-all -v /media/share/mapp/public/QE_plus_unifr/raw/:/data -v /home/allardpm/sandbox:/output chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine msconvert /data/1684941280_PMA_dbgi_000993_01_01_neg.raw --outdir /output

docker run -it --rm -e WINEDEBUG=-all -v /media/share/mapp/public/QE_plus_unifr/raw/:/data -v /home/allardpm/sandbox:/output chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine ls /media/share/mapp/public/QE_plus_unifr/raw/* | xargs -I {} msconvert "{}" --mzML --64 --zlib --outdir /output


ls /media/share/mapp/public/QE_plus_unifr/raw/* | xargs -I {} msconvert "{}" --mzML --64 --zlib


```bash
#!/bin/bash

# Define input and output directories
input_dir="/media/share/mapp/public/QE_plus_unifr/raw/"
output_dir="/home/allardpm/sandbox"

# Find all files in the input directory and process each one
find "$input_dir" -type f | while read file; do
    docker run -it --rm -e WINEDEBUG=-all \
    -v "$input_dir:/data" \
    -v "$output_dir:/output" \
    chambm/pwiz-skyline-i-agree-to-the-vendor-licenses wine msconvert "/data/$(basename "$file")" --outdir /output --mzML --64 --zlib
done
```

