<script setup>
import {ref, computed} from "vue";


const studentName = "Jian Marc Dumadag";
const yearLevel ="3rd Year BSIT";
const school ="Mater Dei College";

const attendance =ref(0);
const present = () =>{
    attendance.value++;
};
const absent = ()=>{
    attendance.value--;
};
const reset = ()=>{
    attendance.value =0;
};

const studentImage ="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTfy576tk0Y8RxFkplXTr_eqdHNYDBpzKEuUITU72HqAK2wGYFu-3XfrRc&s=10";
const schoolLogo ="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5OjcBCgoKDQwNGg8PGjclHyU3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3N//AABEIAJQAmQMBEQACEQEDEQH/xAAcAAACAgMBAQAAAAAAAAAAAAAABgQFAQMHAgj/xABLEAABAwMCAgYGBAoFDQEAAAABAgMEAAUREiEGMQcTQVFxgRQiMmGRoVKxwdEVMzdCQ2JydMLwI3OCkrIXJDQ1NlNUdYOis7ThJf/EABoBAAIDAQEAAAAAAAAAAAAAAAAEAgMFAQb/xAA1EQACAgEDAgIHBwQDAQAAAAAAAQIDEQQhMRJBBXETIjI0UWGRM0KBobHB8AYU0fEjJFLh/9oADAMBAAIRAxEAPwDuNABQAUAFABQAUAFABQB4cWlCSpSgkAZJJ5VGUkllnUsvCFKTxVpuqS160FPqqGN1freXdWNZ4p/z4j7JrV+Gt05ftDVHfbkMpdZWFIUMgitiE1NdUeDJlFwfTLk3VM4FABQAUAFABQAUAFABQAUAFAES6SHYsF19hAcW2NWk9oHP5VVfOUK3KKzgsqipzUW8ZKuFxVb3wA8VsKPPWNviKSq8Uonzsxq3w2+vjdFq1cYTwy1KZX+y4KdjfVLiS+orKqyPMX9Dd17WM9YjH7QqfXH4kemXwND1ygs/jZbCPcXBVcr6o8yRJU2S4iyrmcVQGgQxrkL7kDA+JpO3xKmHs7+Q3X4ddP2tl8xWut7mXIlK1BtnsaRsPPvrG1Ottv24XwNfT6KujflkBKNTSl9ygPiD91K4zHI05eskS7ZdZdtWDHUCgn1m1bpNX6fV2UPMXsUajSV3r1luNULiyG6lPpSFsKI541JP2/KturxOqXtrBj2+G2xfq7lszdIL34qYwr3BwZp2Gopn7MkJyotjzF/QkB9ojIcQfBQqzrj8StxkuxqdnRGhl2SygfrOAVCV1ceZL6ko1zlxF/QrZnE1tYB0OKfUOxpOfnSlviWnr758hqrw++ztglWaa5cYnpS2g2lajoAOTgbZNMaa53Q62sFOoqVU+hPOCxpgoCgAoAKACgDw4gLQpKhkKGCK41lYDLW6OWymTGlPMq5trKfga8bbB1zcH2PXUzVlamu5qwKrLAoDCAADsFGQPSCUqCk7EV2LxujkkmsMkOMJDrKkbMPeyfo74I8j8sVfKC6lJcMXjY+hxftR/mTKGyLZIKhgpfbBHccLrqg1TLzX7g5p3Ra+D/Y8ojFcjqidIQjW6r6Ixk/d41GNWbOnsludldivPdvY0ur6xZUE6U8kjuHdVc31PK4La49Kx37mvAPOoMsM0ZZzCAbcqADBOw59ldSy8I43hZOo25gRYTDCRjQgDz7a9jTBV1qKPI2z65uTJNWkAoAKACgAoAweVAHPuLGepvTqsfjQlfyx9leY8Th06hv4novDZ9WnS+BT1nmiFAHtCwn2kBae0H76nGSWzWSEot7p4ZKjxeuOYKw4vtjubKI7u4+W9Xwq6t6nn5PkWstcNrVj5rg8uPJbjvRQgltwhWleymljY+NDsUYuCW3O/ZnY1uclNvjbPxR4EiS+tbYOovOBakhPtKH8mq/SWSeF33x5E3VVBZfZYz8j2iXracZd9TrXS484BuvuTjs3qcbcxcJd3u/2ISp6Wpx3wtl+57diKQkLl/5s0R6jPtOKHh9pxUpVdO830r82RhdnaHrP48IiLWk7NI0I8ck+J+6l5SX3VgZhF8ye54qBYFBwnWRj0m7RWzy6wKPlv9lM6OvrvivmLayfRRJnSk8q9ceWPVABQAUAFABQBg8qAE7jprEiI79JCk/Aj76wPGI+tCRt+ES2lEV6xzXAbns86AbNzbC1EELZHdl1I+s1bGuXZr6lUrI43T+hLTFWG1KcTDWACrKZCQrywd/hTCqkk21H8GLSti3hOX02K8qKjqUSonmc86Sby8sdSwsIYbHbVRUouMoYcO0VntWs8jj+e+tfRaToxdPnsjJ12rVmaocd2Vl+S2i7yUsgBIXvj6Xb880nrsK+XSO6NydC6jLbC3WEupETKhkrekDWT4E7V2NUpR6kl+L3IOyMZuOX+C2IzkZYJJcYJ/VeSfqNUyred2vqhiNseyf0ZpIwcHHlVTRankxXDpe8Gta7zq/3bSlfZ9prS8KjnUZ+CM3xSWKMfFj4OVelPPGaACgAoAKACgAoAV+O0j0SKv6LuPiP/lY/jCXo4y+DNTwpv0kl8UJvZWAb7CgAGM75x7qFg484NyXkIGzDZOOayVH7vlVinFcRKnXJvLl9CTYmmXbk0JA1NoClqGPa0gnHyq7RQjO9dXHP0KtbNwofTz/kenEspC5SFIU6tOllajsNtgPE16WXTjrT8jza6s9L/E5/NiyYriPS0qS46Cs558yD9Xzry19VkGvScs9PRbXZHFfCNYdToCVsNqI21DIJqPXHGHEn6N5bUjWcfm5A95qt4zsTWe5iuEgxRk4M/AqcypS+5AT862vB160pfIyPF5erFDnW8YgUAFABQAUAFABQArdIV7k2G0MSorbLilSEtqQ8nKVJIJ+yrqaY3ScZcFGoulTHqiJEfjWxTDi6WZyIo/pYbmoH+ycfbVWo8Bqm9jtHjtsOS1jN2W5kfgm+x1LPJmQOrX8/urGv8BthvFmzR47XPaSMyrJcYwyuMpaPptesPlWXZodRXzHPkaleuos4ljzIBGCQQQRzBFKtNcjaaZ6ZdWw8l1o6VpOQa7Cbg+qJGcFOPSz2qU91KmELUlgq1BoHIB7MVOV0+lxT25wQjRDKbW/B7nzn57ja5CgShAQMdw+2pX3zvacuxyjTwoTUe5GqjkuylyTotnuErHUxXMH85Q0j4mma9HfZ7MRazWUV+1I9yYlrtv8Arm9xY5H6Js9Ys+Q+6tSjwK6z2vyMy/xymG0V9Sqk8YcOQdrfa5FwWPz5K9CPhvn4VsUeA1w3l+ZjX+PWT2iM/RzxJJ4gcuHXsR2G2Or6ttlONIOeffypq/TQoSUSjT6md7bkO9LjQUAFABQAUAFAEabOjQW0OSnkNJWtLaSo4yonAHia6k5PCOSkorLOc9KFw9M4WtqipsrclHWG1hQQoJV6uR2jkffTujjix5ENbNOtY+Jy6tMygwO6gCytt/u1qI9AuElpI/M6wqR/dO1VTphPlFsL7IcSGSL0iy1jRebbCnpxjXo6tfxGR8hSN/hVFvYfp8VuqfJZxr/wncjguTLW4ex1OtHkRn7Kx7/6ejzDbyNej+oJcT/MsUWmM5GVMZvVuXAScKk9cNKfcezPnWW/BblPpyaa8apcOvBAlXjhO2/jJkm5uj8yIkBJ/tHH11o0f093mZ1/9QdoFZJ6Q1sgpsloiROwOPDrF/YPrrZp8Joq7GPd4tfYLty4mvd0z6bc5CkH9GhZQn4JwDT8KK4cIQnfZPllSNuVWlIV0EdC6I5aYyr0VuttBLKF9Y6rCU7q3J7qz9cs9JoaGWOo6fa7mzPaIQtHXNpT17aVZ6tSkg4PxpCUXHk0oTUlsT6iTCgAoAKACgBL47cW49GjaHlslJLiRH9IaWc7JWgbg7ZSrvBG1X0rliuoe+BO6Q0GJYOHYpGnIdc0aEI0+zgYRsOfv8TTej3nJims2hFCJT5nhQAHbmRQBtVHfQ2HFsOpbPJamyAfM1FST4ZJxa5Rq8a72IjfbAP8mN4z/wAc3/DSti/7MfIch7tLzFCmxMKACgAoAKAHPouSXrrc4qVEdfb14wEncKT2KBHb27Unrdop/Mc0O8mvkNnBSnY106jqXWmlNnU2mKI7SFd5wTrWcbaTgAbUnd7OR2htSwdBpYcCgAoAKAMGgDnPHhjm+gP+i9aYwSnrOubWUknIGj8cnOPU559xpqjPS8CWoa6v5/GU3Ss2G2OH0BGlKYywE6AjGNG2kbDw7KY0PMvwF9dxH8Tn9PmeABJAAJOeztrjeEdSy8HaeCOGINlQgOoS/dFNJW+tSQeoz+aD2fbjNZF90pvK4NnTURhH5if0ocSpus9FtjfiIaiXFBWQtzltjuGR4k91NaOnpXXIT1l6nLpj2Eanewl3G+2/kxvH783/AA0tP3mPkNw92l5i7aLZIusxqPHSrSpxttbuklLetQSCfdk1dOyMI5YvXXKcsI6bw/0e2iTZlIuLClTm3XWlyGXVjdKiMgZx8qzrNXYpZjwaVejrcMS5KezdHCneIZsS4PKMGIU4UjZT+oZH7OO2rZ6z1E0t2VQ0X/I1J7Ik8Y8CQWXWk2RtMVLUV6Q/rcW4VhBTgDJO+9Rp1cvvbkrtHHPqHOJMd6K+tiS0tp5Gy21jBSffWimpLKM5xcXhjj0Sb8VO45ehOZ/vIpTXfZLzG9D9o/Iu+HUxmuKYjaBFS+246Eo0O9YgEHVhr2Ws7ZVyPZ7VLWdXo/8AQzXj0nP6nTxSY+ZoAKACgDBrjAReOUuC5Mht18dcwUltqehrVg7kpUMgYO60HIB8KZo3QpqNmLvSEkSuE+HpzXVlDeprU2hSEHKRjSFb6fU2zzGKY0jxZJC2rXVVGRzytEzx54B4JXdwm5z1ux2GnkqaRox1wBBzk/mnlkUjqNV0erEd02lc/WkW/HkO+WS1uKhTnXocp9bkxaGSHApW+VKGcIAASOWABVOmdc5esi/UqyuPqPZnL+wCtTjYygo7HUN9t/JjeP35v+GlZ+8x8huHu0vM2dGw/p5n9dC/9hNQ1fC/H9CWk7+a/U6zYP8AR5X77I/8hrOnyjUh3MQf9d3X/o/4TXJeyji9tkDiT/SH/wDlMr/EipQ/cjPl+RyDjn/a65/1o/witbT/AGSMfU/asv8AomaKJ11nlJ0x4mj1U6juc8u32eVUa2W0YjGiW8pfAvODwpy8REh8ltKFOhtE5PVEY2KG8dYpPreyo4TnHYKWt2iM1bzydIpUdCgAoAKACgBa42t5lW1t1DXWqYcCij0dp3bkTheOXuINWUy6XuU3QysiwuKu88LXazqDipjOJTIc3cJzzWeQKilQCRyTimE1XapfEWlF2VOJyxvQpSCvdskZPurUfGxlrnc+m2A2GkBvSEBI06eWOzFef7noo8HiWGjGeDunqyhWvVyxjfPurq5CXDyfM5wFEJ5A7eFb64POPlmK72BDfbfyY3j9+b/hpWfvMfIbh7tLzNnRxqCrk4lOQ16K6oagPVQ8FKOSQOQ76hq+Ir+cEtJt1ZLqR0iNWqQ83b2xKbU8txSFY2KjkgLBwdz2A1THSSlu9i6WsUHhHpfSXDYXKlxIbrkiRow04dIRpBBye33YoWim9nwD1sN2j1D4vZvxfS4dM16I5GZYAS2PXwealb+yO3yqM9PKvyJQ1MbfMS+Ohji+6e50D/tFPaf7JCOp+1Y28OxTaOBQVJPpN4e1ITqKCpAGwSoeyvSCpOeZpO+Ssu8huiPRTnuxm4HgONLmTXW3EqdIRlcZppTmNyolGVE5PafAVRdJPCQzRH7w4VQMhQAUAFABQBplsNyo7jD6EONOJ0qQtIUCPeDzoTxucaysHNupe4buuspDbEValhYjIZaS2cal4Ss61FKdI2GM8t6cyrI4/wBiOHVLP+hb484f9Ckfhi3t/wD58s5Wkb+jOnmhWOW+fq7qZ01vUuiXKFNTSovrhwyoicT32HHQxEu0ltlAwlAUCEjzq+VFUnloqjqLUsKQTOJr7Njrjy7rKdZWMKQVAAju2FcjRXF5SB32SWGypq4pCjsdQ3238mN4/fm/4aVn7zHyG4e7S8xTS64hpxpC1BtzGtIOArHLPfimMJ4bFMvdHipHAoAPHl3d9GMnfIY+FLE9xJdC/OdUILBSZUlxWxAxhGT2kYHuHlS19qqhiPPYZopdssvgbrg47e7gEw2FdVtHbQI6HUpSk4KHG1LTuhSSQruV20nH1I7jks2PY6FabezbIDMSOhtCGxybbDYJ7TpGwzSspOTyx2MelYJtRJBQAUAFABQAUAUnEljaubKXGkoRMa3bd6ltSv2cqBwKnCfS/kVWV9W/cTLbOVa3X4U1pL8NWoS46l9b1Yw4446tQGCpSikYphx6l1Lb+cCsZOOz4Ky+9H3XNGfwu6JDCsExFL9dGQDgHt5jY7+NXVav7thTbo8rqqEWTHeiPKYlMuMup2KHEFKh5GnoyUllCMouLw0aqkRCudjqG+2/kxvH783/AA0tP3mPkNw92l5ihTQmFAHptC3XA22hS1q9lCUkk+AFcbSWWdSbeEO3DvR3MlaZV+c/B8MYJQpQDiu4dyfPek7dYltDkdp0be89kXNynRnITVptbCI1p06UoWSgSAesbcQVYOFAhKgT20vFPPXLkZk1jpjx+o18MWH0M+mzUhyase0420Vtj9tKRnNL2T6tlwMVV9O75GQbVWXBQAUAFABQAUAFAFBxpc5lntBnwkoWptY1IWNlDB+3Fcw20k8HG0k21kQ5HG1nvzSUXqC8w6BhLiFFxv35RkBXnmm/7e+rdLK+Ql/cae32nh/MveF7gwzJUq3XRibGeWVuNuOBDhUoj18EADAGMDPjVM5x4ksMvrhJbweUN1zs9vu7AbuUNmQnsK07p8DzFRjOUPZeCc64zXrIQ7z0WxHSV2aeWDnIZkesnyVzHzpyGtktprIlZoYv2HgSrpwbf7WCt63reaT+kjf0iflv8RTcNTVLbInPTWw3wT7YR/kxvG/Kc3/DUJv/ALMSyPu0l8yptPC97u4CoVvdLZ5OuDQjxyeY8KtnqK4csphp7Z8IdbP0VjZy9z/FmL9qj91KWa58QQ5XoFzNj7ZuHrVZkYtsFllXa5pys+KjvSU7Zz3kx6FMIeyhe4zuTKwuLKnx4kNOyh1oLjh9UggAHGCORG9Fcop7LLOWxk1u8IVm+MbRZnXHrVFely1kkvryyhWeZKAcE53zimPQX2rddK+Yv/cUVbJ5fyHbgG8zr/DkTpuhKSsIbbQNk43PjzFKyg4ScW84G65qcVJLGRqrhMKACgAoAKACgAoAWOkG4QYnDshqa5gvp0tpHMnINCjKUlGPJGclCLlLg4mmEhsR3FvNuBaStxAO6QBnB+qtD+7lOU4dOGsJPzM1aSNahNyTTy2vI9QJkeNNZkuRMlpWdIUcH3YPZ51Zbp7Zw6evPmQqvqjLqcMeR0+B0p210BMuK4ydhlJ1D6hikZae5fd+m4/HVUv7312Mxbnwm8rK5/PPqra1DdercgEbH66i5SXKx+DJKEJd8/ii7s8uxQir0e6sEK7CoJ7vD41W55LIw6SeZ1jVqJlQTqUFqypG6hyPjXOr5nelGm53SyyYqmH7lHCSQdlg7g58+XKhTSeQccrArvyeE4w2ujiyk5wG85x3kjB9/ftnlVinJ8IqdcY7tmyR0mWmGyliEw6/1aQkFasbeIzmpx090uI/sReppjzL9zm18urF2uj0/wBD0reOdOrA/nPvpynT3QjjqwI3302Pq6cmhqI3JcKkutsIU11gzyyNiBv7j8qhLVSojhpyecfPzJx00b5bNRWM/LyOq9FN0hOWUW9tWmU0SVoVzVsNx8KTujKNj6lzv9R2iUZVrp7bD2DkVAuM0AFABQAUAFAHledO3Og4zl/GPBnEF2mqmKfbk/RQ2cBI7gk8viau093osvGSjUUu7G+MCFPgSrSHWJza2nnCE6FAg6Qck4IH6tPV2/3Fi22Rn2VOip5e7N0NNpkNNNvktOpbHWL6zQFK1kHGQdwjB957sVdJ2ReUUx9G1g3R7A3Kx1M5KAWQ8CpIJKcJzsDturHf6p54xUfTtbNHfQp8MhRLNMlxkyI6W1pUnVjVhQGojOPFJ8t6nK6MXiRXGqUllGfwPNCtCQ3rHV+r1oz6/s1xzqZNQsXB4TbZy0tqbAWHAlSdDqTsokDkdtwR5Gj/AIu6/L/4dxd2f5v/ACZNqmeqSprSUhZX1ySlKSlSgSc7DSkmhSqRxxtf+zMiyzI0VUp1CA0jGVJVnYkAHbsOQR3iuq6DeERdUksslvcPKjtvdZNjBSWyWjrGlawojTk8s4PnUfT9XCJ+hxyzY41w/GS8luUp9SkuBC1JJ07jRsNicas+I5dhm1/I7iqJX22G/cwmHFRrfC8oSkEkgjBwPED41XfZ6G30mNmsfiWUw9NX6NPdPP1Hbhzo/vceU3L9JENaDkFR3Hu0jn5kUlqNQ7l0tDun03oX1Z/wdXYS4lpAdUFOADUoDAJ78dlLjZsoAKACgAoAKACgDGKAEvingKPfJjk1Mx1t5Z5HdI2AwPh76nXbOreLKraYWr1kJFw6Nr3G1FgNyEjtQr+T8qch4g/vR+glPw5L2ZfUXpdhu0FX+cQXmiDnOnHwNMLWUvl48yiWiujws+RFC5sbASZLWnYDKgBz5f3j8T31NWUz4aKfR2w7M9fhKaHAv0hepOjBONtJJT8CSfM1PprZzrsT7mGbnLZwG3sYbDYyAcAEkYzyIJODzGa664yD0skYRPlo09W+pOkJAx3JBAHwUoeZocIdzinPsC3psnUFuSXdZOpPrKByc/Xiq3OqG+UiXo7ZbJP8yRFst1mr/oIT7pJ+jmq5a2hcPPkXLRXvlY8y/t/RzfZZBdbbjJPatW/w51RLX/8AiP1Lo+H/APuX0HPhvo7ZtMxia9NcXIaII6sYHPOPDypO2+d3tMcp09dXsr+foPgGKgXmaACgAoAKACgAoAKACgAoAKAMEAjGKAIr1ugvfjYcdee9sVxpPk71NcENzhuyue3bY5/s4owcyaTwrYtWPwYz8T99GATNrfDVlb9i2RxjvTmudKO5ZMZtkBoDq4UdPg2K6kgy2SwABgAAd1dOGaACgAoAKACgAoAKAP/Z";
const width = 120;
const height = 120;

const student = [
    {id:1, name:"Jian", course:"BSIT"},
    {id:2, name:"Aljon", course:"BSIT"},
    {id:3, name:"Alanie", course:"BSIT"},
    {id:4, name:"Harvey", course:"BSIT"}

];

const isEnrolled =true;
const gpa = ref(1.0);

const gpa1 = 1.5;
const gpa2 = 2.4;
const gpa3 =1.9;

const averageGpa = computed(()=>{
return ((gpa1 + gpa2+ gpa3) /3).toFixed(2);
}
);


</script>


<template>
    <div>
     
        <h1>{{ studentName }}</h1>
        <h2>Year Level: {{ yearLevel }}</h2>
        <h2>Studying at {{ school }}</h2>
<h1>Attendance:{{ attendance }}</h1>
        <button @click="present">Present</button>
        <button @click="absent">Absent</button>
        <button @click="reset">Reset</button>
        <h2>Student Id</h2>
        
        <img
        :src ="studentImage"
        :width="width"
        :height="height"/>

        <h2>School logo</h2>
        <img
        :src ="schoolLogo"
        :width="width"
        :height="height"/>

</div>
<div v-for="stud in student" :key="stud.id">
   {{ stud.id }}
   {{ stud.name }}
   {{ stud.course }}

   
</div>

<div>
<h3>Status: {{ isEnrolled ? "Enrolled" : "Not enrolled"}}</h3>
   
        
</div>

<div>
 <h3>GPA: {{ gpa }}</h3>
    <p v-if="gpa >= 1.0 ">Excellent</p>
    <p v-else-if="gpa <= 2.0">Good</p>
    <p v-else>Needs Improvements</p>
    <h3>{{ gpa1 }},
        {{ gpa2 }},
        {{ gpa3 }}
    </h3>
    <h3>Average: {{ averageGpa }}</h3>
</div>

</template>


