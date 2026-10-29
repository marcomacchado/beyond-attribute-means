# Input data

Obtain MGPHot from the dataset authors' release:

- Dataset: https://zenodo.org/records/15372063
- Paper: Sergio Oramas, Fabien Gouyon, Steve Hogan, Camilo Landau and Andreas Ehmann (2025). *MGPHot: A Dataset of Musicological Annotations for Popular Music (1958–2022).* https://doi.org/10.5334/tismir.236

Place these files directly in this directory:

```text
data/
  mgphot_genes.tsv
  mgphot_gene_values.tsv
```

Use the files from the data release with their original row order. The notebook reads `name` and `category` from the gene metadata and `gene_values` and `year` from the track file. The 58-element vectors must use the metadata's attribute ordering. No chart-position file is needed.

The data used for this paper have 21,299 tracks across 1958–2022. The expected SHA-256 hashes are:

```text
mgphot_genes.tsv
2d4b7f6edf0c5cdbbd3924cdfb37d2ba1715b6c54c937fc153d5e5c1139d9582

mgphot_gene_values.tsv
0be32e1bda5e5d33a43d676275ee1f26bf2ef9b9373e8d29fb63faf149cedb8b
```

The raw dataset is not bundled in this code package. Refer to its original release for the applicable data terms and citation. Downloading a different version or changing row order can affect resampling results even if the number of tracks is unchanged.
