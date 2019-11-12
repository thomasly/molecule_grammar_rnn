1. Install rdkit (chemical informatics, http://www.rdkit.org/docs/Install.html) using Anaconda. 

2. Install pytorch. The project uses pytorch 0.3.1, later versions are not backward compatible and will not run.

3. First prepare data by running `python -m data data/zinc.smi` (Generate samples from pretrained VAE for testing the grammar model)

4. To train your own VAE. `python -m vae --restore vae-pretrained --generate-samples`

5. Train grammar_rnn model, the main paper contribution. This takes approximately ten minutes. `python -m grammar_model`