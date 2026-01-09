# Chimera-linux-bore-rt
Just tried to port some patches from cachy os bore rt kernel to chimera linux, feels a little bit snapier ( mostly for zen3 architecture )


# How to compile ( just copy for automated process )
git clone https://github.com/chimera-linux/cports && \
cd cports && \
./cbuild keygen && \
./cbuild bootstrap && \
rm -rf main/linux-stable && \
cd main && \
git clone https://github.com/BedrockMC/Chimera-linux-bore-rt && \
mv Chimera-linux-bore-rt linux-stable &&\
cd .. &&\
./cbuild pkg main/linux-stable

# Note, if you want to compile on zen 4 or 5
Change the file in cports/main/linux-stable/template.py all znver3 to znver4 or znver5 ( depending on your processor generation )
