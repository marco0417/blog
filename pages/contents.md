- #+BEGIN_QUERY
  {:title "Recenlty"
   :query [:find (pull ?b [*])
           :in $ ?start ?today ?tag
           :where
           (between ?b ?start ?today)
           (page-ref ?b ?tag)]
   :inputs [:7d-before :today "今日见闻"]}
  #+END_QUERY