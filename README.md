# SFO Air Traffic Passenger Statistics – Airline Clustering

Unsupervised learning on the **Air Traffic Passenger Statistics** dataset for San Francisco International Airport (SFO), July 2005 – June 2018 (18,885 monthly records).

**Research question:** *Which airlines have similar air-traffic characteristics?*

## Approach
- Records without an IATA airline code (ground handlers and non-airline operators) removed.
- Raw records aggregated to **one row per airline**; airlines with fewer than 12 months of data excluded (65 airlines retained).
- Features: log average monthly passengers, domestic share, low-fare share, transit share and long-haul share.
- **K-Means** clustering, with the number of clusters chosen by the Elbow Method and silhouette analysis (silhouette 0.70).
- An initial model with eight separate regional shares showed no clear elbow; consolidating them into a single long-haul share produced a clearer, more interpretable structure.

## Six airline profiles
1. Smaller domestic carriers
2. Long-haul international carriers
3. Domestic low-fare carriers
4. Non-long-haul international carriers
5. Large domestic / network carriers
6. Domestic carriers with transit activity

## Files
- `sfo-air-traffic-passenger-clustering.ipynb` – full notebook with code, charts and cluster profiles

## Tools
Python · pandas · scikit-learn · matplotlib · seaborn

---
Part of my [data science portfolio](https://betulcelep.github.io/#data-science), completed during the *Mastering Applied Data Science with Deep Learning* programme.
