This is a Resume builder project. It renders your information onto html template with an ability to download PDF file.<br/>
if you have troubles with installing wkhtmltopdf on windows, try including the full path to wkhtmltopdf in views.py file inside the download_link view, like so:<br/>
config = pdfkit.configuration(wkhtmltopdf='C:\Program Files\wkhtmltopdf\bin\wkhtmltopdf.exe')<br/>
and then you add config to pdfkit function like so:<br/>
pdf = pdfkit.from_string(html, False, options, css=css, configuration=config)<br/>
