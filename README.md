#Socketstream passport rpc middleware

###Usage example
 --- passport.coffee middleware ---

 passport    = require 'passport'
 ssPassport  = require 'ss-passport-request'

 exports.initialize = (options = {}) ->
   return passport.initialize()     
  
 exports.session = (options = {}) ->
   return passport.session()
  
 exports.req = (options = {})->
   return ssPassport


 --- usage example ---
 when creating rpc use
 
 req.use "session"
 req.use "passport.initialize"
 req.use "passport.session"
 req.use "passport.req"
