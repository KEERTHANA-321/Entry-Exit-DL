## Entry Exit DL

A Django application to record the entry and exit of students into the library by scanning their ID cards using an RFID reader.

### System Requirements

- Python 3.7 or above
- Git
- RFID Reader with compatible RFID cards
- Ubuntu 20.04 or higher (for Linux installation) or Windows 10/11 (for Windows installation)
- Access to the same network for both the server and the RFID reader

### Installation

#### Ubuntu

1. Update package lists:

```bash
sudo apt update
```

2. Install required packages:

```bash
sudo apt install git python3-pip python3-virtualenv
```

3. Clone the repository:

```bash
git clone https://github.com/AfthabEK/Entry-Exit-DL.git
cd Entry-Exit-DL
```

4. Create and activate a virtual environment:

```bash
virtualenv venv
source venv/bin/activate
```

5. Install the project dependencies:

```bash
pip3 install -r requirements.txt
```

6. Configure the RFID reader IP in `views.py` inside the `enter` folder.

7. Run the Django development server:

```bash
python3 manage.py runserver
```

#### Windows

1. Install Python 3.x from the official website: https://www.python.org/downloads/

2. Install Git for Windows from: https://git-scm.com/download/win

3. Open a command prompt or Git Bash.

4. Clone the repository:

```bash
git clone https://github.com/AfthabEK/Entry-Exit-DL.git
cd Entry-Exit-DL
```

5. Create and activate a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

6. Install the project dependencies:

```bash
pip install -r requirements.txt
```

7. Configure the RFID reader IP in `views.py` inside the `enter` folder.

8. Run the Django development server:

```bash
python manage.py runserver
```

### Usage

1. Ensure the RFID reader is connected and accessible on the same network as the server.


To add the usage instructions and additional information to the README file, you can include the following sections:

## Usage

1. Put the card on the RFID reader.

2. Open your web browser and go to `localhost:8000` or `http://your-server-ip:8000`.

   ![Homepage](screenshots/homepage.png)

3. Click on the "Submit" button after the RFID reader successfully reads the card.

   - Successful Read and Student Entry:
   ![Successful Entry](screenshots/entry_success.png)

   - Successful Read and Student Exit:
   ![Successful Exit](screenshots/exit_success.png)

   - Failed Read:
   ![Failed Read](screenshots/failed_read.png)

4. To view all records, click on the "View Records" link from the navigation menu.

   ![View Records](screenshots/view_records.png)

5. To see the list of students currently inside, click on the "Current Records" link from the navigation menu.

   ![Current Records](screenshots/current_records.png)

6. To view the list of students who entered today, click on the "Records for Today" link from the navigation menu.

   ![Records for Today](screenshots/records_today.png)

6. To view the list of students on a specific day, click on the "View by Date" link from the navigation menu.

7. To view the list of students for a specific month, click on the "View by Month" link from the navigation menu.

8. To download student data for a specific date, click on the "Download by Date" link from the navigation menu.

9. To download student data for a specific month, click on the "Download by Month" link from the navigation menu.

### Admin Tasks

To clear the database and delete all data, run the `clear.py` script. **Warning**: Make sure to backup data by downloading it before running this script.

### Notes
This software was made for the [eSSL U-5 RFID reader](https://www.esslsecurity.com/rfidreaders/u-5).
![eSSL U-5 RFID reader](screenshots/essl-u5.jpg)
 If you are using a different device, please make sure to modify the readData
function in [views.py](/enter/views.py).

## Contribution
Contributions are always welcome! Feel free to create a pull request, and I'll review it promptly.
