# Data Cleaning Report

Raw dataset: **30000 rows**, **10 columns**.

## 1. Missing values found (before cleaning)

No missing values found.

## 2. Outliers detected (IQR method, before capping)

'price' is checked **per location** (a single global IQR would wrongly flag genuinely expensive metro-city houses as outliers, since price levels differ a lot by city). 'area_sqft' is checked globally.

**Price outliers by location:**

| location       |   lower_bound |   upper_bound |   n_outliers |
|:---------------|--------------:|--------------:|-------------:|
| Ahmedabad      |  -2.32062e+07 |   7.37018e+07 |            0 |
| Amritsar       |  -2.36826e+07 |   7.47704e+07 |            0 |
| Bangalore      |  -2.27359e+07 |   7.35471e+07 |            0 |
| Bhopal         |  -2.04625e+07 |   7.19815e+07 |            0 |
| Bhubaneswar    |  -2.49916e+07 |   7.54554e+07 |            0 |
| Bilaspur       |  -2.447e+07   |   7.508e+07   |            0 |
| Chennai        |  -2.18425e+07 |   7.24815e+07 |            0 |
| Coimbatore     |  -2.08949e+07 |   7.24961e+07 |            0 |
| Cuttack        |  -2.29828e+07 |   7.31092e+07 |            0 |
| Dehradun       |  -2.1668e+07  |   7.3788e+07  |            0 |
| Durgapur       |  -2.50895e+07 |   7.57805e+07 |            0 |
| Dwarka         |  -2.63648e+07 |   7.88772e+07 |            0 |
| Faridabad      |  -2.32722e+07 |   7.24498e+07 |            0 |
| Gaya           |  -2.4374e+07  |   7.5738e+07  |            0 |
| Gurgaon        |  -2.25995e+07 |   7.37545e+07 |            0 |
| Guwahati       |  -2.2721e+07  |   7.3807e+07  |            0 |
| Haridwar       |  -2.58728e+07 |   7.66712e+07 |            0 |
| Hyderabad      |  -2.06238e+07 |   7.48802e+07 |            0 |
| Indore         |  -2.30672e+07 |   7.32628e+07 |            0 |
| Jaipur         |  -2.37755e+07 |   7.45005e+07 |            0 |
| Jamshedpur     |  -2.379e+07   |   7.2986e+07  |            0 |
| Jodhpur        |  -2.33918e+07 |   7.47422e+07 |            0 |
| Kochi          |  -2.18549e+07 |   7.31621e+07 |            0 |
| Kolkata        |  -2.0371e+07  |   7.2069e+07  |            0 |
| Lucknow        |  -2.29864e+07 |   7.33726e+07 |            0 |
| Ludhiana       |  -2.61779e+07 |   7.56671e+07 |            0 |
| Mangalore      |  -2.36012e+07 |   7.37508e+07 |            0 |
| Mumbai         |  -2.48445e+07 |   7.66955e+07 |            0 |
| Mysore         |  -1.93604e+07 |   7.19326e+07 |            0 |
| Nagpur         |  -2.5675e+07  |   7.6389e+07  |            0 |
| New Delhi      |  -2.26836e+07 |   7.31394e+07 |            0 |
| Noida          |  -2.2668e+07  |   7.5232e+07  |            0 |
| Patna          |  -2.16795e+07 |   7.22765e+07 |            0 |
| Pune           |  -2.18265e+07 |   7.20235e+07 |            0 |
| Raipur         |  -2.3597e+07  |   7.4659e+07  |            0 |
| Ranchi         |  -2.31485e+07 |   7.24635e+07 |            0 |
| Silchar        |  -2.50394e+07 |   7.61296e+07 |            0 |
| Surat          |  -2.64345e+07 |   7.52495e+07 |            0 |
| Trivandrum     |  -2.16385e+07 |   7.17255e+07 |            0 |
| Vijayawada     |  -2.343e+07   |   7.3786e+07  |            0 |
| Vishakhapatnam |  -2.7141e+07  |   7.8311e+07  |            0 |
| Warangal       |  -2.4147e+07  |   7.6353e+07  |            0 |

**area_sqft** (global): 0 outlier(s) outside [-1758, 7254]

## 3. Cleaning actions taken

- Removed 0 duplicate rows (30000 -> 30000 rows).
