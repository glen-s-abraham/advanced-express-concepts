#################EXPERESS GENERATOR###################
npm i -g express-generator
express - generate express project
npm i
#################NCONF CONFIGURATION LIBRARY###################
npm i nconf

nconf.argv(options) Loads process.argv using optimist
nconf.env(options) Loads process.env into hierarchy
nconf.file(options) Loads congig data from fileinto hierarchy
nconf.defaults(options) Loads data in options into hierarchy
nconf.override(options) Loads data in options into hierarchy.s

Defaults>file>argv>env>overrides

const nconf = require('nconf')

--console arguements

nconf.argv({
'p':{
'alias':'http:port',
'describe':'The port to listen on'
}
})

node ./bin/www -p 8002

--environment variable with delimiter
nconf.env('\_\_')

--config file
nconf.file('config.json')

--defaults
nconf.defaults({
"http":{
"port":3000
}
})

app.set('port', nconf.get('http:port'));

#################WINSTON LOGGER###################
npm i winston
winston.info()
winston.silly()
winston.debug()
winston.verbose()
winston.warn()
winston.error()

winston.add(new winston.transports.File({ filename: 'logfile.log',level:'error' }));
