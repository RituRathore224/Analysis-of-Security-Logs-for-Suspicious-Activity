# Analysis-of-Security-Logs-for-Suspicious-Activity
How many login failures happened? Out of 500 total login records, 80 were failed attempts and 420 were successful, meaning about 16% of all logins failed — a notable share worth investigating further.

Which username had the most failed attempts? The user lpetrov had the highest number of failed login attempts, with 14 failures — significantly more than other users, making this account a top concern.

Which IP address appears most often? The IP 192.168.5.45 was the most frequently seen address, appearing 16 times across the logs.

At what time did suspicious activity increase? Failed login attempts spiked around 3 AM, with 10 failures recorded in that hour alone — a strong indicator of automated or off-hours attack activity, since legitimate users rarely log in at that time.

Is there a brute-force attack pattern? Yes. Two username-IP combinations crossed the brute-force threshold (5+ failed attempts from the same IP): lpetrov from IP 141.98.11.100 — 10 failed attempts dwilliams from IP 103.219.145.9 — 7 failed attempts This is a classic brute-force signature — the same account being repeatedly targeted from a single external IP.

Are there many failures before a success? Not significantly. On average, successful logins took only ~1.14 attempts, with a maximum of 2 attempts before success. This suggests most successful logins are legitimate first-or-second-try logins, not the result of a drawn-out brute-force success.

Did one account show too many access attempts? Yes — lpetrov also had the highest total activity overall, with 35 access attempts (success + failed combined), far above the average user, reinforcing that this account is the most targeted or compromised.

Which device or host shows unusual behavior? The device DESKTOP-B77 recorded the most failed login attempts (17), making it the most suspicious endpoint in the dataset.

Were there repeated logins from different locations? Yes — nearly all users logged in from multiple locations (6–9 different locations each), with dwilliams and lpetrov topping the list at 9 locations apiece. This kind of geographic spread, especially combined with their high failure counts, suggests possible credential sharing, VPN abuse, or account compromise.

Overall Conclusion: The account lpetrov stands out as the primary suspect for suspicious activity — it has the most failed attempts, the highest total access volume, was targeted in a clear brute-force pattern from IP 141.98.11.100, and logged in from 9 different locations. Combined with the after-hours spike at 3 AM and device DESKTOP-B77's high failure count, the data points to a coordinated brute-force attempt against a small set of accounts rather than random, scattered failures.

