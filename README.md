# gitconfig-aliases
My git config aliases

Running the following command should add the new aliases in your .gitconfig file:
```bash
cp ~/.gitconfig ~/.gitconfig.backup && \
(grep "\[alias\]" ~/.gitconfig > /dev/null || echo -e "\n[alias]" >> ~/.gitconfig) && \
curl -s https://raw.githubusercontent.com/aaron777collins/gitconfig-aliases/main/.gitconfig | \
sed -n '/^\[alias\]/,/^$/p' | \
grep -v "^\[alias\]" >> ~/.gitconfig
```

Note that this assumes your aliases are at the bottom of the file. You may want to verify it works.
