# MP3 – Secret Scanning Evaluation

Evaluates and compares three secret scanning tools against the `leaky-repo` benchmark dataset.

## Project Structure

```
secret-scanning/
|-- dataset/
     |-- leaky-repo/
|-- results/
     |--detect-secrets.json
     |-- credsweeper.json
     |-- semgrep.txt
|-- README.md
|-- slides.pptx


---

## Tools Used


| detect-secrets | `pip install detect-secrets` |
| CredSweeper | `pip install credsweeper` |
| Semgrep | `pip install semgrep` |

---

## Setup

```bash
python -m venv venv
.\venv\Scripts\Activate        # Windows
pip install detect-secrets credsweeper semgrep
```


---

## Run the Scanners

```bash
# detect-secrets
cd .\dataset\leaky-repo
detect-secrets scan > ..\..\results\detect-secrets.json  #the output of it is saved in the result folder
cd ..\..

# CredSweeper
credsweeper --path .\dataset\leaky-repo > .\results\credsweeper.json   # the output of it is saved in the result folder

# Semgrep
semgrep scan --config=auto .\dataset\leaky-repo > .\results\semgrep.txt  # the output of it is saved in the resut folder
```


---
