
# Cleanup 

rm -rf cnijfilter2-5.70-1-rpm.tar.gz pkg scangearmp2-3.70-1-rpm.tar.gz src

# Make

makepkg

# Install

makepkg -i
