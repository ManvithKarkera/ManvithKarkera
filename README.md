## Manvith Karkera

Computer Engineering student at Fr. Conceicao Rodrigues College of Engineering, Mumbai (graduating 2028, CGPA 9.29/10). I mostly work on backends and cloud setups, and I like testing my projects against real data.

Looking for software or backend internships for winter 2026 and summer 2027, remote or in Mumbai.<br>
Email: [manvith.karkera176@gmail.com](mailto:manvith.karkera176@gmail.com) · [LinkedIn](https://www.linkedin.com/in/manvith-karkera-176f)

---

### PitWall: F1 lap telemetry analyzer on AWS
[Code](https://github.com/ManvithKarkera/pitwall) · FastAPI, React, PostgreSQL, AWS, CloudFormation

<a href="https://github.com/ManvithKarkera/pitwall"><img src="assets/pitwall.jpg" alt="PitWall comparing Russell and Hamilton" width="720"></a>

Pick two F1 drivers' laps and see where the time was gained or lost. It overlays speed, throttle, brake and gear, shows the running gap, and colours the track map by who was faster in each mini-sector.

- The API puts each comparison on an SQS queue. A worker on EC2 processes the telemetry and saves the charts and a PDF report to S3. A failed job is retried 3 times and then goes to a dead-letter queue, which sets off an alarm.
- All the AWS resources come from one CloudFormation template. The database is in private subnets, IAM permissions are kept tight, and there's no SSH port open.
- The numbers match official timing. For 2024 Monza qualifying it shows Norris 0.134 s ahead of Leclerc, which is the official gap.

### note2recall: flashcards from your own lecture notes
[Live](https://note2recall.vercel.app) · [Code](https://github.com/ManvithKarkera/note2recall) · Python, spaCy, scikit-learn, Sentence-Transformers, FastAPI, React

Upload lecture PDFs (scanned ones work too, through OCR) and get flashcards. Each card links back to the sentence and page it came from. It uses classic NLP and runs locally, with no LLM calls.

- Every answer is taken directly from its source sentence.
- On two real lecture decks (78 and 118 pages), a 20-card deck covers 68 to 96% of the top 25 concepts.
- Duplicate detection with sentence embeddings gets an F1 of 0.80. TF-IDF gets 0.56.

### SYN Flood Virtual Lab
[Code](https://github.com/ManvithKarkera/css_mini) · JavaScript, Node.js tests

A browser lab where you watch a SYN flood fill up a server's TCP connection queue, then turn on SYN cookies, rate limiting or firewall filtering and watch it recover. I led a team of 5 and wrote the simulation engine.

### Other work
- [Hack Into PCell](https://github.com/41vi4p/Hack_Into_PCell_ESP32): I wrote the ESP32 firmware (C/C++) for a 15-node offline treasure hunt on campus. Each node runs its own Wi-Fi hotspot, web server and team login.
- The Project Cell website for Fr. CRCE (Next.js, Vercel), used by 200+ students.

---

Languages: Python, C, C++, JavaScript, TypeScript, Java, SQL<br>
Backend and cloud: FastAPI, PostgreSQL, AWS, Docker, Linux, pytest<br>
ML and NLP: spaCy, scikit-learn, Sentence-Transformers, Pandas, NumPy<br>
Embedded: ESP32, Arduino
