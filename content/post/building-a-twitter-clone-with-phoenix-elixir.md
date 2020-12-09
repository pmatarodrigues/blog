+++
authors = []
date = 2020-08-22T22:19:00Z
excerpt = "Phoenix is a web development framework written in Elixir which implements the Model – View – Controller (MVC) pattern. Phoenix is a lot of times compared with other web frameworks like Ruby on Rails and Django"
hero = "/uploads/flutter-705x3971.png"
timeToRead = 0
title = "Building a Twitter Clone with Phoenix (Elixir)"

+++
> _(Work in Progress)_
>
> This blog post is being updated as i'm progressing through the project and implementing new features and learning new things

## Preparing Project

### Install latest Phoenix version (from github, with special features)

`$ git clone `[`https://github.com/phoenixframework/phoenix.git`](https://github.com/phoenixframework/phoenix.git "https://github.com/phoenixframework/phoenix.git")  
`$ cd phoenix/installer`  
`$ mix archive.install`

### Create the project (**tuita** is project's name)

`$ mix phx.new `**`tuita`**` --live`

### Configure project

**Timeline** is the main field, which will be composed of **Tuites** (called _tuites_ on the database, and will contain the fields marked as bold on the command (username, body, fav_count and retuite_count).

`$ mix phx.gen.live Timeline Tuite tuites `**`username body fav_count:integer retuite_count:integer`**

### Add live routes to scope

    live "/tuites", TuiteLive.Index, :index
    live "/tuites/new", TuiteLive.Index, :new
    live "/tuites/:id/edit", TuiteLive.Index, :edit
    
    live "/tuites/:id", TuiteLive.Show, :show
    live "/tuites/:id/show/edit", TuiteLive.Show, :edit

### Create and migrate Database

`$ mix ecto.create`

`$ mix ecto.migrate`

### Running server

`$ mix phx.server`

Now we visit **localhost:4000** and there it is, our newly (and ridiculously fast) created blog style website with live update. As simple as that.

![](https://ementa.test/wp-content/uploads/2020/09/image.png)

## Project Structure

* _build
* assets
* config
* deps
* **lib**
  * **tuita**
    * **timeline** (the one we previously set as the main container)
      * tuite.ex (configuration of each tuite)
    * (...)
  * **tuita_web**
    * controllers
    * live
      * _here we can configure each components presentation format_
    * templates
    * views
    * (...)
  * tuita.ex
  * tuita_web.ex
* priv
* test
* (...)

## Input Validation

After removing the unnecessary fields from **form_component.html.leex** and leaving just the body, proceeding to the validation of those fields on **tuite.ex**. Adding validation is as simple as modifying the following lines on that file:

      @doc false
      def changeset(tuite, attrs) do
        tuite
        |> cast(attrs, [:body])
        |> validate_required([:body])
        |> validate_length(:body, min: 2, max: 275)
      end

## Live Updates

![](https://ementa.test/wp-content/uploads/2020/09/ezgif.com-video-to-gif.gif =702x369)

Working with this Phoenix's [**LiveView **](https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html)module allows us to automatically render the page with the newly created data, without the need to completely refresh the page. Using LiveView, only the necessary data is passed on this broadcast, keeping the internet usage pretty low.

### Resources

Gigalixir

* [https://hexdocs.pm/phoenix/gigalixir.html](https://hexdocs.pm/phoenix/gigalixir.html "https://hexdocs.pm/phoenix/gigalixir.html")

> _(Work in Progress)_
>
> This blog post is being updated as i'm progressing through the project and implementing new features and learning new things