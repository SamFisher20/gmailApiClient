# gmailApiClient

Explore the seamless integration of Gmail within a Spring Boot framework with this application, designed to offer secure and efficient email management. Harnessing OAuth2 for robust authentication, it provides a user-friendly platform to read, compose, and organize emails, making it an ideal solution for both personal and professional email interactions powered by Gmail's extensive capabilities.

## Getting Started with the Gmail API

### Setting Up Google Services

1. **Create a Project in Google Cloud Console**:
   - Navigate to the [Google Cloud Console](https://console.cloud.google.com/).
   - Create a new project.
   - *Note*: Remember the Project ID as it will be used later.

2. **Enable the Gmail API**:
   - In the Google Cloud Console, navigate to "APIs & Services" > "Dashboard."
   - Click "+ ENABLE APIS AND SERVICES" and search for "Gmail API."
   - Enable the Gmail API for your project.

3. **Create Credentials**:
   - Go to "APIs & Services" > "Credentials."
   - Click "Create Credentials" and select "OAuth client ID."
   - Set up the OAuth consent screen if prompted.
   - Choose "Web application" as the Application type.
   - Add the necessary redirect URIs (e.g., `http://localhost:8080/login/oauth2/code/google` for local testing).
   - *Note*: Keep the Client ID and Client Secret secure.

### Configuring Application Credentials

To integrate the Gmail API with your Spring Boot application, you need to configure your Google credentials in the `application.yaml` file. This allows your application to authenticate with Google services securely.

1. **Locate or Create Your `application.yaml`**:
   - Find the `application.yaml` file in your Spring Boot project's `src/main/resources` directory.
   - If the file doesn't exist, create it in the aforementioned directory.

2. **Add Google Credentials**:
   - Open `application.yaml` and add the following lines, replacing `YOUR_CLIENT_ID` and `YOUR_CLIENT_SECRET` with your actual Google OAuth 2.0 credentials:

    ```yaml
    google:
      client-id: YOUR_CLIENT_ID
      client-secret: YOUR_CLIENT_SECRET
    ```

3. **Referencing Credentials in the Application**:
   - In your Spring Boot application, reference these credentials using the `@Value` annotation or through configuration properties binding.
   - Example for using `@Value`:

    ```java
    @Value("${google.client-id}")
    private String googleClientId;

    @Value("${google.client-secret}")
    private String googleClientSecret;
    ```

4. **Securing the Credentials**:
   - **Important**: Do not commit the `application.yaml` file with real credentials to public repositories. Consider using environment variables or external configuration management for sensitive data.

### Setting Up Spring Boot Application

1.    **Initialize a Spring Boot Project**:
        - Use Spring Initializr to bootstrap a new Spring Boot project.
        - Choose the necessary dependencies (e.g., Spring Web etc) and add it to build.gradle file.

2.    **Clone/Download the Project**:
        - git clone <your-repository-url>
        - Or download the ZIP file and extract it.

3.    **Open and Run the Project**:
        - Open the project in your preferred IDE.
        - Run the application (usually by running the main method in the YourApplication.java file).

## Tech Stack

This project utilizes the following technologies:

- **Gmail API & Service**
- **Google API**
- **Spring Boot**
- **OAuth2**

## What I Learned

During the development of this project, I gained experience in:

- Integrating Gmail API with a Spring Boot application.
- Managing OAuth2 authentication and authorization flow.
- Application development using Spring Boot.

## Future Enhancements

Here are some ideas for future enhancements and features for the project:

| Feature                        | Description                               | 
| ------------------------------ | ----------------------------------------- | 
| Advanced Email Filtering       | Implement more complex email filtering.   | 
| Email Scheduling               | Add functionality to schedule emails.     | 
| UI Improvements                | Enhance the user interface for ease of use. |
| Integration with Other APIs    | Integrate with other Google APIs for extended functionality. | 
| Automated Testing Suite        | Develop a comprehensive testing suite.    |

*Your contributions and suggestions are welcome!*

## Contributing

Contributions to this project are welcome! Here's how you can contribute:

1. **Fork the Repository**: Click the 'Fork' button at the top-right corner of this page.
2. **Clone Your Fork**: `git clone https://github.com/your-username/project-name.git`
3. **Create a New Branch**: `git checkout -b your-new-feature`
4. **Make Changes and Commit**: Make your changes and commit them with a clear commit message.
5. **Push to Your Fork**: `git push origin your-new-feature`
6. **Create a Pull Request**: Open a new pull request from your fork to the main project.
