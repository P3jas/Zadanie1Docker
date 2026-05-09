Zgodnie z wymaganiami, obraz został sprawdzony pod kątem obecności zagrożeń. Do analizy wykorzystano narzędzie Trivy.
Początkowa wersja obrazu zawierała podatności typu HIGH. Zostały one wyeliminowane
poprawiony dockerfile wzgledem pierwszego jest pod nazwa Dockerfile_dod

Finalny obraz zad1pogoda:1.9 nie zawiera żadnych podatności klasyfikowanych jako HIGH lub CRITICAL (wynik: 0 - Clean).
<details>
<summary>Logi z terminala</summary>

```bash

pejas@Kacper1:/mnt/d/kody/PROJEKT CHMURY$ docker run --rm -v /var/run/docker.sock:/var/run/docker.sock aquasec/trivy image zad1pogoda:1.9
2026-05-09T10:09:09Z    INFO    [vulndb] Need to update DB
2026-05-09T10:09:09Z    INFO    [vulndb] Downloading vulnerability DB...
2026-05-09T10:09:09Z    INFO    [vulndb] Downloading artifact...        repo="mirror.gcr.io/aquasec/trivy-db:2"
351.22 KiB / 92.47 MiB [>____________________________________________________________] 0.37% ? p/s ?1.22 MiB / 92.47 MiB [>______________________________________________________________] 1.32% ? p/s ?2.27 MiB / 92.47 MiB [->_____________________________________________________________] 2.45% ? p/s ?3.42 MiB / 92.47 MiB [->________________________________________________] 3.70% 5.13 MiB p/s ETA 17s4.61 MiB / 92.47 MiB [-->_______________________________________________] 4.98% 5.13 MiB p/s ETA 17s5.75 MiB / 92.47 MiB [--->______________________________________________] 6.22% 5.13 MiB p/s ETA 16s6.94 MiB / 92.47 MiB [--->______________________________________________] 7.50% 5.18 MiB p/s ETA 16s8.09 MiB / 92.47 MiB [---->_____________________________________________] 8.75% 5.18 MiB p/s ETA 16s9.25 MiB / 92.47 MiB [---->____________________________________________] 10.00% 5.18 MiB p/s ETA 16s10.11 MiB / 92.47 MiB [----->__________________________________________] 10.93% 5.19 MiB p/s ETA 15s10.67 MiB / 92.47 MiB [----->__________________________________________] 11.54% 5.19 MiB p/s ETA 15s11.61 MiB / 92.47 MiB [------>_________________________________________] 12.55% 5.19 MiB p/s ETA 15s12.73 MiB / 92.47 MiB [------>_________________________________________] 13.77% 5.13 MiB p/s ETA 15s14.22 MiB / 92.47 MiB [------->________________________________________] 15.38% 5.13 MiB p/s ETA 15s15.94 MiB / 92.47 MiB [-------->_______________________________________] 17.24% 5.13 MiB p/s ETA 14s18.44 MiB / 92.47 MiB [--------->______________________________________] 19.94% 5.42 MiB p/s ETA 13s21.64 MiB / 92.47 MiB [----------->____________________________________] 23.40% 5.42 MiB p/s ETA 13s24.33 MiB / 92.47 MiB [------------>___________________________________] 26.31% 5.42 MiB p/s ETA 12s25.08 MiB / 92.47 MiB [------------->__________________________________] 27.12% 5.78 MiB p/s ETA 11s26.31 MiB / 92.47 MiB [------------->__________________________________] 28.46% 5.78 MiB p/s ETA 11s28.78 MiB / 92.47 MiB [-------------->_________________________________] 31.13% 5.78 MiB p/s ETA 11s31.16 MiB / 92.47 MiB [---------------->_______________________________] 33.69% 6.06 MiB p/s ETA 10s33.70 MiB / 92.47 MiB [----------------->_______________________________] 36.45% 6.06 MiB p/s ETA 9s36.50 MiB / 92.47 MiB [------------------->_____________________________] 39.47% 6.06 MiB p/s ETA 9s37.42 MiB / 92.47 MiB [------------------->_____________________________] 40.47% 6.34 MiB p/s ETA 8s38.00 MiB / 92.47 MiB [-------------------->____________________________] 41.09% 6.34 MiB p/s ETA 8s38.28 MiB / 92.47 MiB [-------------------->____________________________] 41.40% 6.34 MiB p/s ETA 8s40.93 MiB / 92.47 MiB [--------------------->___________________________] 44.27% 6.31 MiB p/s ETA 8s42.12 MiB / 92.47 MiB [---------------------->__________________________] 45.55% 6.31 MiB p/s ETA 7s43.34 MiB / 92.47 MiB [---------------------->__________________________] 46.87% 6.31 MiB p/s ETA 7s44.34 MiB / 92.47 MiB [----------------------->_________________________] 47.95% 6.27 MiB p/s ETA 7s45.29 MiB / 92.47 MiB [------------------------>________________________] 48.98% 6.27 MiB p/s ETA 7s45.93 MiB / 92.47 MiB [------------------------>________________________] 49.68% 6.27 MiB p/s ETA 7s45.93 MiB / 92.47 MiB [------------------------>________________________] 49.68% 6.04 MiB p/s ETA 7s47.57 MiB / 92.47 MiB [------------------------->_______________________] 51.45% 6.04 MiB p/s ETA 7s47.57 MiB / 92.47 MiB [------------------------->_______________________] 51.45% 6.04 MiB p/s ETA 7s49.62 MiB / 92.47 MiB [-------------------------->______________________] 53.66% 6.04 MiB p/s ETA 7s50.17 MiB / 92.47 MiB [-------------------------->______________________] 54.25% 6.04 MiB p/s ETA 6s52.31 MiB / 92.47 MiB [--------------------------->_____________________] 56.57% 6.04 MiB p/s ETA 6s53.18 MiB / 92.47 MiB [---------------------------->____________________] 57.52% 6.04 MiB p/s ETA 6s54.00 MiB / 92.47 MiB [---------------------------->____________________] 58.39% 6.04 MiB p/s ETA 6s55.17 MiB / 92.47 MiB [----------------------------->___________________] 59.66% 6.04 MiB p/s ETA 6s56.56 MiB / 92.47 MiB [----------------------------->___________________] 61.16% 6.01 MiB p/s ETA 5s57.60 MiB / 92.47 MiB [------------------------------>__________________] 62.30% 6.01 MiB p/s ETA 5s58.43 MiB / 92.47 MiB [------------------------------>__________________] 63.19% 6.01 MiB p/s ETA 5s58.62 MiB / 92.47 MiB [------------------------------->_________________] 63.39% 5.84 MiB p/s ETA 5s58.68 MiB / 92.47 MiB [------------------------------->_________________] 63.46% 5.84 MiB p/s ETA 5s60.03 MiB / 92.47 MiB [------------------------------->_________________] 64.92% 5.84 MiB p/s ETA 5s61.40 MiB / 92.47 MiB [-------------------------------->________________] 66.40% 5.77 MiB p/s ETA 5s61.57 MiB / 92.47 MiB [-------------------------------->________________] 66.59% 5.77 MiB p/s ETA 5s62.50 MiB / 92.47 MiB [--------------------------------->_______________] 67.59% 5.77 MiB p/s ETA 5s63.21 MiB / 92.47 MiB [--------------------------------->_______________] 68.36% 5.59 MiB p/s ETA 5s63.95 MiB / 92.47 MiB [--------------------------------->_______________] 69.16% 5.59 MiB p/s ETA 5s64.85 MiB / 92.47 MiB [---------------------------------->______________] 70.14% 5.59 MiB p/s ETA 4s66.37 MiB / 92.47 MiB [----------------------------------->_____________] 71.78% 5.57 MiB p/s ETA 4s67.18 MiB / 92.47 MiB [----------------------------------->_____________] 72.65% 5.57 MiB p/s ETA 4s67.18 MiB / 92.47 MiB [----------------------------------->_____________] 72.65% 5.57 MiB p/s ETA 4s67.89 MiB / 92.47 MiB [----------------------------------->_____________] 73.42% 5.37 MiB p/s ETA 4s68.54 MiB / 92.47 MiB [------------------------------------>____________] 74.12% 5.37 MiB p/s ETA 4s70.18 MiB / 92.47 MiB [------------------------------------->___________] 75.90% 5.37 MiB p/s ETA 4s70.18 MiB / 92.47 MiB [------------------------------------->___________] 75.90% 5.27 MiB p/s ETA 4s70.48 MiB / 92.47 MiB [------------------------------------->___________] 76.22% 5.27 MiB p/s ETA 4s71.93 MiB / 92.47 MiB [-------------------------------------->__________] 77.79% 5.27 MiB p/s ETA 3s73.09 MiB / 92.47 MiB [-------------------------------------->__________] 79.04% 5.24 MiB p/s ETA 3s73.87 MiB / 92.47 MiB [--------------------------------------->_________] 79.89% 5.24 MiB p/s ETA 3s74.54 MiB / 92.47 MiB [--------------------------------------->_________] 80.61% 5.24 MiB p/s ETA 3s74.87 MiB / 92.47 MiB [--------------------------------------->_________] 80.97% 5.10 MiB p/s ETA 3s75.79 MiB / 92.47 MiB [---------------------------------------->________] 81.97% 5.10 MiB p/s ETA 3s76.96 MiB / 92.47 MiB [---------------------------------------->________] 83.23% 5.10 MiB p/s ETA 3s77.62 MiB / 92.47 MiB [----------------------------------------->_______] 83.94% 5.06 MiB p/s ETA 2s78.28 MiB / 92.47 MiB [----------------------------------------->_______] 84.65% 5.06 MiB p/s ETA 2s78.57 MiB / 92.47 MiB [----------------------------------------->_______] 84.97% 5.06 MiB p/s ETA 2s79.71 MiB / 92.47 MiB [------------------------------------------>______] 86.21% 4.96 MiB p/s ETA 2s80.42 MiB / 92.47 MiB [------------------------------------------>______] 86.97% 4.96 MiB p/s ETA 2s81.40 MiB / 92.47 MiB [------------------------------------------->_____] 88.03% 4.96 MiB p/s ETA 2s82.48 MiB / 92.47 MiB [------------------------------------------->_____] 89.20% 4.94 MiB p/s ETA 2s83.14 MiB / 92.47 MiB [-------------------------------------------->____] 89.91% 4.94 MiB p/s ETA 1s84.12 MiB / 92.47 MiB [-------------------------------------------->____] 90.97% 4.94 MiB p/s ETA 1s85.12 MiB / 92.47 MiB [--------------------------------------------->___] 92.05% 4.91 MiB p/s ETA 1s85.73 MiB / 92.47 MiB [--------------------------------------------->___] 92.71% 4.91 MiB p/s ETA 1s86.65 MiB / 92.47 MiB [--------------------------------------------->___] 93.71% 4.91 MiB p/s ETA 1s87.15 MiB / 92.47 MiB [---------------------------------------------->__] 94.25% 4.81 MiB p/s ETA 1s87.90 MiB / 92.47 MiB [---------------------------------------------->__] 95.06% 4.81 MiB p/s ETA 0s88.73 MiB / 92.47 MiB [----------------------------------------------->_] 95.96% 4.81 MiB p/s ETA 0s89.59 MiB / 92.47 MiB [----------------------------------------------->_] 96.89% 4.76 MiB p/s ETA 0s90.48 MiB / 92.47 MiB [----------------------------------------------->_] 97.85% 4.76 MiB p/s ETA 0s91.07 MiB / 92.47 MiB [------------------------------------------------>] 98.49% 4.76 MiB p/s ETA 0s92.18 MiB / 92.47 MiB [------------------------------------------------>] 99.69% 4.73 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.73 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.73 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.46 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.46 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.46 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.17 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.17 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 4.17 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.90 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.90 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.90 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.65 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.65 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.65 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.41 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.41 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.41 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.19 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.19 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 3.19 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 2.99 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 2.99 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 2.99 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [----------------------------------------------->] 100.00% 2.79 MiB p/s ETA 0s92.47 MiB / 92.47 MiB [---------------------------------------------------] 100.00% 4.15 MiB p/s 22s2026-05-09T10:09:32Z INFO    [vulndb] Artifact successfully downloaded       repo="mirror.gcr.io/aquasec/trivy-db:2"
2026-05-09T10:09:32Z    INFO    [vuln] Vulnerability scanning is enabled
2026-05-09T10:09:32Z    INFO    [secret] Secret scanning is enabled
2026-05-09T10:09:32Z    INFO    [secret] If your scanning is slow, please try '--scanners vuln' to disable secret scanning
2026-05-09T10:09:32Z    INFO    [secret] Please see https://trivy.dev/docs/v0.70/guide/scanner/secret#recommendation for faster secret detection
2026-05-09T10:09:35Z    INFO    [python] Licenses acquired from one or more METADATA files may be subject to additional terms. Use `--debug` flag to see all affected packages.
2026-05-09T10:09:35Z    INFO    Detected OS     family="alpine" version="3.23.4"
2026-05-09T10:09:35Z    INFO    [alpine] Detecting vulnerabilities...   os_version="3.23" repository="3.23" pkg_num=38
2026-05-09T10:09:35Z    INFO    Number of language-specific files       num=1
2026-05-09T10:09:35Z    INFO    [python-pkg] Detecting vulnerabilities...

Report Summary

┌──────────────────────────────────────────────────────────────────────────────────┬────────────┬─────────────────┬─────────┐
│                                      Target                                      │    Type    │ Vulnerabilities │ Secrets │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ zad1pogoda:1.9 (alpine 3.23.4)                                                   │   alpine   │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/blinker-1.9.0.dist-info/METADATA        │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/certifi-2026.4.22.dist-info/METADATA    │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/charset_normalizer-3.4.7.dist-info/MET- │ python-pkg │        0        │    -    │
│ ADATA                                                                            │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/click-8.3.3.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/flask-3.1.3.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/idna-3.13.dist-info/METADATA            │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/itsdangerous-2.2.0.dist-info/METADATA   │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/jinja2-3.1.6.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/markupsafe-3.0.3.dist-info/METADATA     │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/requests-2.33.1.dist-info/METADATA      │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/urllib3-2.7.0.dist-info/METADATA        │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ root/.local/lib/python3.11/site-packages/werkzeug-3.1.8.dist-info/METADATA       │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/backports.tarfile-1.2.0.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/jaraco_context-6.1.2.dist-info/METADATA   │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/packaging-26.2.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/pip-26.1.1.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools-82.0.1.dist-info/METADATA      │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/autocommand-2.2.2.dis- │ python-pkg │        0        │    -    │
│ t-info/METADATA                                                                  │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/backports.tarfile-1.2- │ python-pkg │        0        │    -    │
│ .0.dist-info/METADATA                                                            │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/importlib_metadata-8.- │ python-pkg │        0        │    -    │
│ 7.1.dist-info/METADATA                                                           │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/jaraco.text-4.0.0.dis- │ python-pkg │        0        │    -    │
│ t-info/METADATA                                                                  │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/jaraco_context-6.1.0.- │ python-pkg │        0        │    -    │
│ dist-info/METADATA                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/jaraco_functools-4.4.- │ python-pkg │        0        │    -    │
│ 0.dist-info/METADATA                                                             │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/more_itertools-10.8.0- │ python-pkg │        0        │    -    │
│ .dist-info/METADATA                                                              │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/packaging-26.0.dist-i- │ python-pkg │        0        │    -    │
│ nfo/METADATA                                                                     │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/platformdirs-4.4.0.di- │ python-pkg │        0        │    -    │
│ st-info/METADATA                                                                 │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/tomli-2.4.0.dist-info- │ python-pkg │        0        │    -    │
│ /METADATA                                                                        │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/wheel-0.46.3.dist-inf- │ python-pkg │        0        │    -    │
│ o/METADATA                                                                       │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/setuptools/_vendor/zipp-3.23.0.dist-info- │ python-pkg │        0        │    -    │
│ /METADATA                                                                        │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.11/site-packages/wheel-0.47.0.dist-info/METADATA           │ python-pkg │        0        │    -    │
└──────────────────────────────────────────────────────────────────────────────────┴────────────┴─────────────────┴─────────┘
Legend:
- '-': Not scanned
- '0': Clean (no security findings detected)

pejas@Kacper1:/mnt/d/kody/PROJEKT CHMURY$
```
</details>




Zbudowano obraz kontenera zgodny z OCI przeznaczony na platformy sprzętowe linux/arm64 oraz linux/amd64.
Poprawność publikacji obrazu wieloplatformowego została potwierdzona za pomocą polecenia docker buildx imagetools inspect. Manifest zawiera poprawne deklaracje dla obu wymaganych platform sprzętowych.

<details>
<summary>Logi z terminala</summary>

```bash
pejas@Kacper1:/mnt/d/kody/PROJEKT CHMURY$ docker buildx build \
  --platform linux/amd64,linux/arm64 \
  -t pejas/laboratoria:zad1pogoda-multi \
  --cache-to type=inline \
  --push .
[+] Building 9.8s (27/27) FINISHED                                                                                                                                          docker-container:moj-builder
 => [internal] load build definition from Dockerfile                                                                                                                                                0.0s
 => => transferring dockerfile: 930B                                                                                                                                                                0.0s
 => [linux/amd64 internal] load metadata for docker.io/library/python:3.11-alpine                                                                                                                   1.1s
 => [linux/arm64 internal] load metadata for docker.io/library/python:3.11-alpine                                                                                                                   1.1s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                                                                       0.0s
 => [internal] load .dockerignore                                                                                                                                                                   0.0s
 => => transferring context: 79B                                                                                                                                                                    0.0s
 => [linux/amd64 builder 1/5] FROM docker.io/library/python:3.11-alpine@sha256:8b5bfdb1fd2d78aa94e21c4d61be52487693f54be7f1021647751ff365795703                                                     0.0s
 => => resolve docker.io/library/python:3.11-alpine@sha256:8b5bfdb1fd2d78aa94e21c4d61be52487693f54be7f1021647751ff365795703                                                                         0.0s
 => [internal] load build context                                                                                                                                                                   0.0s
 => => transferring context: 92B                                                                                                                                                                    0.0s
 => [linux/arm64 builder 1/5] FROM docker.io/library/python:3.11-alpine@sha256:8b5bfdb1fd2d78aa94e21c4d61be52487693f54be7f1021647751ff365795703                                                     0.0s
 => => resolve docker.io/library/python:3.11-alpine@sha256:8b5bfdb1fd2d78aa94e21c4d61be52487693f54be7f1021647751ff365795703                                                                         0.0s
 => CACHED [linux/arm64 builder 2/5] WORKDIR /app                                                                                                                                                   0.0s
 => CACHED [linux/arm64 stage-1 3/6] RUN apk update && apk upgrade --no-cache &&     pip install --no-cache-dir --upgrade pip setuptools wheel jaraco.context                                       0.0s
 => CACHED [linux/arm64 builder 3/5] COPY requirements.txt .                                                                                                                                        0.0s
 => CACHED [linux/arm64 builder 4/5] RUN pip install --no-cache-dir --upgrade pip setuptools wheel jaraco.context                                                                                   0.0s
 => CACHED [linux/arm64 builder 5/5] RUN pip install --no-cache-dir --user -r requirements.txt                                                                                                      0.0s
 => CACHED [linux/arm64 stage-1 4/6] COPY --from=builder /root/.local /root/.local                                                                                                                  0.0s
 => CACHED [linux/arm64 stage-1 5/6] COPY main.py .                                                                                                                                                 0.0s
 => CACHED [linux/arm64 stage-1 6/6] COPY tlo.jpg .                                                                                                                                                 0.0s
 => CACHED [linux/amd64 builder 2/5] WORKDIR /app                                                                                                                                                   0.0s
 => CACHED [linux/amd64 stage-1 3/6] RUN apk update && apk upgrade --no-cache &&     pip install --no-cache-dir --upgrade pip setuptools wheel jaraco.context                                       0.0s
 => CACHED [linux/amd64 builder 3/5] COPY requirements.txt .                                                                                                                                        0.0s
 => CACHED [linux/amd64 builder 4/5] RUN pip install --no-cache-dir --upgrade pip setuptools wheel jaraco.context                                                                                   0.0s
 => CACHED [linux/amd64 builder 5/5] RUN pip install --no-cache-dir --user -r requirements.txt                                                                                                      0.0s
 => CACHED [linux/amd64 stage-1 4/6] COPY --from=builder /root/.local /root/.local                                                                                                                  0.0s
 => CACHED [linux/amd64 stage-1 5/6] COPY main.py .                                                                                                                                                 0.0s
 => CACHED [linux/amd64 stage-1 6/6] COPY tlo.jpg .                                                                                                                                                 0.0s
 => exporting to image                                                                                                                                                                              8.4s
 => => exporting layers                                                                                                                                                                             0.0s
 => => preparing layers for inline cache                                                                                                                                                            0.0s
 => => exporting manifest sha256:8fd9882946b79ac34e03e2967a1a57757f7ec61eb60b6090823063945c0c7002                                                                                                   0.0s
 => => exporting config sha256:fabbe2a746da6a7d5e138c74e82f820c066c3c2f5a3a382f60fe62ec0ebd26a2                                                                                                     0.0s
 => => exporting attestation manifest sha256:03ff75bb15e7c6e6d4413540265c06e17ccdfe25bea766d46246973b41371f0c                                                                                       0.0s
 => => exporting manifest sha256:2b7e8be260835bf1723158ef6b141c8176303e055cf6dec718891f44a2be1159                                                                                                   0.0s
 => => exporting config sha256:7e32e066e240151e1ab1ec06acaec2bf893fb4c70244ebd53d18205e41399c71                                                                                                     0.0s
 => => exporting attestation manifest sha256:3dbf9e5be6e77bd650ab48e506c31d5be47e65186f2052aca36844328fb1e243                                                                                       0.0s
 => => exporting manifest list sha256:458d396f4f190b75da7217240b409790d37311fb69a02c40a5063e7c81d8bac9                                                                                              0.0s
 => => pushing layers                                                                                                                                                                               3.3s
 => => pushing manifest for docker.io/pejas/laboratoria:zad1pogoda-multi@sha256:458d396f4f190b75da7217240b409790d37311fb69a02c40a5063e7c81d8bac9                                                    5.0s
 => [auth] pejas/laboratoria:pull,push token for registry-1.docker.io                                                                                                                               0.0s
 => [auth] pejas/laboratoria:pull,push pejas/zad1pogoda:pull token for registry-1.docker.io                                                                                                         0.0s
pejas@Kacper1:/mnt/d/kody/PROJEKT CHMURY$ docker buildx imagetools inspect pejas/laboratoria:zad1pogoda-multi
Name:      docker.io/pejas/laboratoria:zad1pogoda-multi
MediaType: application/vnd.oci.image.index.v1+json
Digest:    sha256:458d396f4f190b75da7217240b409790d37311fb69a02c40a5063e7c81d8bac9
           
Manifests: 
  Name:        docker.io/pejas/laboratoria:zad1pogoda-multi@sha256:8fd9882946b79ac34e03e2967a1a57757f7ec61eb60b6090823063945c0c7002
  MediaType:   application/vnd.oci.image.manifest.v1+json
  Platform:    linux/amd64
               
  Name:        docker.io/pejas/laboratoria:zad1pogoda-multi@sha256:2b7e8be260835bf1723158ef6b141c8176303e055cf6dec718891f44a2be1159
  MediaType:   application/vnd.oci.image.manifest.v1+json
  Platform:    linux/arm64
               
  Name:        docker.io/pejas/laboratoria:zad1pogoda-multi@sha256:03ff75bb15e7c6e6d4413540265c06e17ccdfe25bea766d46246973b41371f0c
  MediaType:   application/vnd.oci.image.manifest.v1+json
  Platform:    unknown/unknown
  Annotations: 
    vnd.docker.reference.digest: sha256:8fd9882946b79ac34e03e2967a1a57757f7ec61eb60b6090823063945c0c7002
    vnd.docker.reference.type:   attestation-manifest
               
  Name:        docker.io/pejas/laboratoria:zad1pogoda-multi@sha256:3dbf9e5be6e77bd650ab48e506c31d5be47e65186f2052aca36844328fb1e243
  MediaType:   application/vnd.oci.image.manifest.v1+json
  Platform:    unknown/unknown
  Annotations: 
    vnd.docker.reference.digest: sha256:2b7e8be260835bf1723158ef6b141c8176303e055cf6dec718891f44a2be1159
    vnd.docker.reference.type:   attestation-manifest
pejas@Kacper1:/mnt/d/kody/PROJEKT CHMURY$ 
```
</details>
