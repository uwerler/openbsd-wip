# $OpenBSD$

COMMENT =		ncurses file manager with vi keybindings
DISTNAME =		vifm-0.10
CATEGORIES =		sysutils
HOMEPAGE =		https://vifm.info/

MAINTAINER =		Rafael Sadowski <rsadowski@openbsd.org>

# GPLv2+
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += X11 c curses m magic pthread

MASTER_SITES =		${MASTER_SITE_SOURCEFORGE:=vifm/}
EXTRACT_SUFX =		.tar.bz2

SEPARATE_BUILD =	Yes

LIB_DEPENDS =		devel/libmagic
RUN_DEPENDS =		devel/desktop-file-utils

CONFIGURE_STYLE =	gnu
CONFIGURE_ARGS =	--with-libmagic \
			--without-gtk \
			--without-dyn-X11

CONFIGURE_ENV =		CPPFLAGS="-I${X11BASE}/include -I${LOCALBASE}/include" \
			LDFLAGS="-L${X11BASE}/lib -L${LOCALBASE}/lib"

.include <bsd.port.mk>
