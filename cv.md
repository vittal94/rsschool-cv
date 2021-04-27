# My cv
## Personal info
- name: *Vitaly Nepom*
- telegram: *@VittalyN*
- email: *evg994z@mail.ru*

## About me
I am begginer programmer looking for opportunity to ingage in android development.That is why i joined this course.  I hope, that it  will improove me 
a lot in my goal to be an android developer.

## My skills
- Java core
- Android dev (some pet projects)
- Android Studio
- Gradle
- English A1

# My examples code
This is code from my e learning android project that currently under development.

```java
public class MainAdapter extends RecyclerView.Adapter<MainAdapter.ViewHolder> {
    List<VerticalData> list;
    Context context;
    public MainAdapter(List<VerticalData> list,Context context){
        this.list = list;
        this.context = context;
    }
    @NonNull
    @Override
    public ViewHolder onCreateViewHolder(@NonNull ViewGroup parent, int viewType) {
        return new ViewHolder(LayoutInflater.from(parent.getContext()).inflate(R.layout.chapter_layout,parent,false));
    }

    @Override
    public void onBindViewHolder(@NonNull ViewHolder holder, int position) {
        holder.title.setText(list.get(position).getTitle());

        holder.childRecycler.setAdapter(new ChildAdapter(list.get(position).getItemData()));
        holder.childRecycler.setHasFixedSize(true);

    }

    @Override
    public int getItemCount() 
        return list.size();
    }

    public class ViewHolder extends RecyclerView.ViewHolder{
        TextView title;
        RecyclerView childRecycler;
        public ViewHolder(@NonNull View itemView) {
            super(itemView);
            title = itemView.findViewById(R.id.chapterTitle);
            childRecycler = itemView.findViewById(R.id.ChildRecycler);
        }
    }
}
```
.
