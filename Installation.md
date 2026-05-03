Markdown
**✅ Verify:**

```bash
rustc --version
cargo --version
```
⚡ 2. Install Solana CLI (working method)
```Bash
wget [https://github.com/solana-labs/solana/releases/latest/download/solana-install-init-x86_64-unknown-linux-gnu](https://github.com/solana-labs/solana/releases/latest/download/solana-install-init-x86_64-unknown-linux-gnu)
chmod +x solana-install-init-x86_64-unknown-linux-gnu
./solana-install-init-x86_64-unknown-linux-gnu v1.18.26
```
➕ Add to PATH:

```Bash
export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
echo 'export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
✅ Verify:

```Bash
solana --version
🌐 3. Install Node.js (needed for Anchor)
Bash
curl -o- [https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh](https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh) | bash
source ~/.bashrc
nvm install --lts
```
✅ Verify:

```Bash
node -v
npm -v
```
⚙️ 4. Install system dependencies
```Bash
sudo apt update
sudo apt install build-essential pkg-config libudev-dev libssl-dev -y
```
⚓ 5. Install Anchor CLI
```Bash
cargo install --git [https://github.com/coral-xyz/anchor](https://github.com/coral-xyz/anchor) anchor-cli --locked
⏳ (takes 10–20 min)
```

➕ Fix PATH (important)

```Bash
export PATH="$HOME/.cargo/bin:$PATH"
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
✅ Verify:

```Bash
anchor --version
🔥 6. Final Setup (Solana)
Bash
solana config set --url [https://api.devnet.solana.com](https://api.devnet.solana.com)
solana-keygen new
solana airdrop 2
solana balance
```
✅ FINAL CHECK (everything)
```Bash
rustc --version
solana --version
anchor --version
node -v
```
🎯 You’re Done When:
Rust ✔

Solana CLI ✔

Anchor CLI ✔

Node.js ✔

👉 Now you can build real Solana projects
