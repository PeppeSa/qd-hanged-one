### FOLDER PATHS VARY AS THE DEVELOPMENT ENVIRONMENT CHANGES! ###

# create .pot files with:
cd {project_folder}
python {anaconda_folder}\Tools\i18n\pygettext.py -d base -o .\locales\base.pot .\main.py

# copy base.pot into both {project_folder}\locales\{lang}\LC_MESSAGES and rename it as base.po
# then build .mo files starting from a .po file
cd {project_folder}\locales\{lang}\LC_MESSAGES
python {anaconda_folder}\Tools\i18n\msgfmt.py -o base.mo base