## This library is deprecated. Use new module: https://github.com/jaksab/EasyNetwork

## Global

This tool allows you to quickly and flexibly configure and perform HTTP requests.
Create by Konovalenko Andrew, onCreate company.

## How to use?

- If you want use this project as library:

`check >> Project - Properties - Android - is Library`

- Code example:

```
Net net = new Net(context, Net.METHOD_GET, "https://api.github.com");

net.connect(new ConnectionListener() {
			
			@Override
			public void onStartConnection(String toUrl) {
				
			}
			
			@Override
			public void onFinishConnection(boolean isSuccessful, HttpResponse response,
					String entity, String fromUrl) {
				
			}
		});
```
`void onStartConnection` - called before library send request
`[String toUrl]` - the last address of the request

`void onFinishConnection` - called after library get response
`[boolean isSuccessful]` - request passed or not, if not response and entity equal null
`[HttpResponse response]` - the full data of response pakage (entity, headers etc)
`[String entity]` - the entity data of response pakage
`[String fromUrl]` - the address from the response

######For use json decode functions you must download gson library and include in you project. `https://code.google.com/p/google-gson/downloads/list`

#####See more in DemonstrationActivity in this project.
