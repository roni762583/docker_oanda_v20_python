# oanda_v20_python
# dockerfile for python environment with installed Oanda v20 API samples

# Instructions:

Clone repository

In a terminal, at directory of cloned repo, run:

            docker run -it $(docker build -q .)

- this will build the container according to dockerfile including files from repo


Configuration script needs to be run to setup account token, otherwise, a .v20.conf file is to be placed in the home ~ directory of container
 * for additional information on setup script and conf file format, see: https://github.com/oanda/v20-python-samples
 
To verify it works, run in container prompt from previous step:

            v20-account-summary
            
- this should return summary of active Oanda account based on    .v20.conf    file
