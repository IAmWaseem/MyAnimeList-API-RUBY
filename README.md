#Getting started

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build my_anime_list_api.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install my_anime_list_api-1.0.0.gem ```

![Building Gem](http://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeList%20API-Ruby&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

## How to Use

The following section explains how to use the MyAnimeListAPI Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](http://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](http://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](http://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the MyAnimeListAPI gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'my_anime_list_api', '~> 1.0.0' ```

![Add references of the Gemfile](http://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](http://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](http://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](http://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](http://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### 

API client can be initialized as following.

```ruby

client = MyAnimeListApi::MyAnimeListAPIClient.new
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](http://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=MyAnimeList%20API-Ruby&workspaceName=MyAnimeListAPI&projectName=my_anime_list_api&gemName=my_anime_list_api&gemVer=1.0.0&initLine=client%2520%253D%2520MyAnimeListAPIClient.new)

## Class Reference

### <a name="list_of_controllers"></a>List of Controllers

* [AnimeController](#anime_controller)
* [MangaController](#manga_controller)
* [UserController](#user_controller)

### <a name="anime_controller"></a>![Class: ](http://apidocs.io/img/class.png ".AnimeController") AnimeController

#### Get singleton instance

The singleton instance of the ``` AnimeController ``` class can be accessed from the API Client.

```ruby
anime = client.anime
```

#### <a name="retrieve_an_anime"></a>![Method: ](http://apidocs.io/img/method.png ".AnimeController.retrieve_an_anime") retrieve_an_anime

> Returns a specific Anime.


```ruby
def retrieve_an_anime(anime_id, 
                          mine = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| anime_id |  ``` Required ```  | The id of the anime. |
| mine |  ``` Optional ```  | Include to also retrieve the authenticated user's anime details (e.g. user's score, watched status, watched episodes). Requires authentication. |


#### Example Usage

```ruby
anime_id = 140
mine = true

result = anime.retrieve_an_anime(anime_id, mine)

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 404 | Unexpected error in API call. See HTTP response body for details. |



#### <a name="search_for_an_anime"></a>![Method: ](http://apidocs.io/img/method.png ".AnimeController.search_for_an_anime") search_for_an_anime

> Returns all anime matching query.  Only the following fields are available:
> **id**, **title**, **episodes**, **type**, **synopsis**, **image_url**,
> **members_score**, **start_date**, **end_date**, **classification**


```ruby
def search_for_an_anime(query); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| query |  ``` Required ```  | The query you want to perform |


#### Example Usage

```ruby
query = 'query'

result = anime.search_for_an_anime(query)

```


[Back to List of Controllers](#list_of_controllers)

### <a name="manga_controller"></a>![Class: ](http://apidocs.io/img/class.png ".MangaController") MangaController

#### Get singleton instance

The singleton instance of the ``` MangaController ``` class can be accessed from the API Client.

```ruby
manga = client.manga
```

#### <a name="retrieve_an_anime"></a>![Method: ](http://apidocs.io/img/method.png ".MangaController.retrieve_an_anime") retrieve_an_anime

> Returns a specific Anime.


```ruby
def retrieve_an_anime; end
```

#### Example Usage

```ruby

result = manga.retrieve_an_anime()

```


#### <a name="search_for_an_anime"></a>![Method: ](http://apidocs.io/img/method.png ".MangaController.search_for_an_anime") search_for_an_anime

> Returns all manga matching query


```ruby
def search_for_an_anime; end
```

#### Example Usage

```ruby

result = manga.search_for_an_anime()

```


[Back to List of Controllers](#list_of_controllers)

### <a name="user_controller"></a>![Class: ](http://apidocs.io/img/class.png ".UserController") UserController

#### Get singleton instance

The singleton instance of the ``` UserController ``` class can be accessed from the API Client.

```ruby
user = client.user
```

#### <a name="retrieve_a_user"></a>![Method: ](http://apidocs.io/img/method.png ".UserController.retrieve_a_user") retrieve_a_user

> Returns a specific user.


```ruby
def retrieve_a_user; end
```

#### Example Usage

```ruby

result = user.retrieve_a_user()

```


#### <a name="retrieve_user_history"></a>![Method: ](http://apidocs.io/img/method.png ".UserController.retrieve_user_history") retrieve_user_history

> Returns user's history


```ruby
def retrieve_user_history; end
```

#### Example Usage

```ruby

result = user.retrieve_user_history()

```


[Back to List of Controllers](#list_of_controllers)



