# Steps to install wkhtml in the instance to create a PDF out of json file .

## Follow the following steps 

```

sudo apt purge wkhtmltopdf

# make a directory
mkdir wkhtmltopdf_0-12-5
cd wkhtmltopdf_0-12-5/

# Download
wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb

# Install the package from your downloaded file
sudo apt install ./wkhtmltox_0.12.5-1.bionic_amd64.deb

/usr/local/bin/wkhtmltopdf --version

# might be different to

/usr/bin/wkhtmltopdf --version
```

Source : https://www.stephankoellen.com/blog/wkhtmltopdf-footer-and-header/#:~:text=Wkhtmltopdf%20provides%20the%20handy%20options,This%20should%20work.
