# devops-sample-code

A minimal sample repository used for DevOps practice. It holds a single shell script that is pulled and executed by a Jenkins Freestyle job.

## Contents

| File | Description |
|---|---|
| `hello-world.sh` | Bash script that prints `Hello, Jenkins!` |

## The Script

```bash
#!/bin/bash
echo "Hello, Jenkins!"
```

## Run It Locally

Using Git Bash, WSL, or any Linux/macOS shell:

```bash
git clone https://github.com/lakshyaaa76/devops-sample-code.git
cd devops-sample-code
bash hello-world.sh
```

Expected output:

```text
Hello, Jenkins!
```

## Use It with Jenkins

This repository is the source for the `HelloWorld` Jenkins job.

1. Create a **Freestyle project** named `HelloWorld`.
2. Under **Source Code Management**, select **Git** and set:
   * Repository URL: `https://github.com/lakshyaaa76/devops-sample-code.git`
   * Branch Specifier: `*/main`
3. Under **Build Steps**, add **Execute shell** with:
   ```bash
   sh hello-world.sh
   ```
4. Click **Save**, then **Build Now**.
5. Open the build and click **Console Output**. It should end with:
   ```text
   Hello, Jenkins!
   Finished: SUCCESS
   ```

## Related

The full walkthrough, with screenshots, is in the **8-Jenkins-Hello-World-Job** exercise of the DEVOPSLAB repository.

## Tech

* Bash
* Git / GitHub
* Jenkins